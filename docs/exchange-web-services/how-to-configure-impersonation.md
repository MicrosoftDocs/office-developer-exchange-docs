---
title: "Configure impersonation"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: "Learn how to grant the impersonation role to a service account by using the Exchange Management Shell."
localization_priority: Priority
---

# Configure impersonation

Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.
  
Impersonation enables a caller, such as a service application, to impersonate a user account. The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.
  
Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts. Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.
  
## Configuring the ApplicationImpersonation role

When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:
  
- _Name_ &ndash; The friendly name of the role assignment. Each time that you assign a role, an entry is made in the RBAC roles list. You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.
- _Role_ &ndash; The RBAC role to assign. When you set up impersonation, you assign the **ApplicationImpersonation** role.
- _User_ &ndash; The service account.
- _CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate. The service account will only be allowed to impersonate other users within the specified scope. If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization. You can create custom management scopes by using the [New-ManagementScope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.

Before you can configure impersonation, you need:
  
- Administrative credentials for the Exchange server.
- Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.
- Exchange management tools. These are installed on the computer from which you will run the commands.

### To configure impersonation for all users in an organization

1. Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.
2. Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user. The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.

   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### To configure impersonation for specific users or groups of users

1. Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.
2. Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned. If an existing scope is available, you can skip this step. The following example shows how to create a management scope for a specific group.

   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope. You can use the properties of the **Identity** object to create the filter. The following example is a filter that restricts the result to a single user with the user name "john."

   ```powershell
   Name -eq "john"
   ```

3. Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope. The following example shows how to configure a service account to impersonate all users in a scope.

   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```

After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts. You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.
  
## See also

- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
- [ApplicationImpersonation role](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
- [New-ManagementRoleAssignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)
- [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
