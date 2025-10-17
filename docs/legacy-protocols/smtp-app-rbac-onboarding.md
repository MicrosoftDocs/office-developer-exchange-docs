---
# Required metadata
# For more information, see https://learn.microsoft.com/en-us/help/platform/learn-editor-add-metadata
# For valid values of ms.service, ms.prod, and ms.topic, see https://learn.microsoft.com/en-us/help/platform/metadata-taxonomies

title:       # Add a title for the browser tab
description: # Add a meaningful description for search results
author:      Ian-MSFT-2019 # GitHub alias
ms.author:   iamcdo # Microsoft alias
ms.service:  # Add the ms.service or ms.prod value
# ms.prod:   # To use ms.prod, uncomment it and delete ms.service
ms.topic:    # Add the ms.topic value
ms.date:     10/17/2025
---

# SMTP Onboarding to App RBAC Overview

RBAC for Applications in Exchange Online allows admins to grant permissions to an application that's independently accessing data in Exchange Online. This grant can be paired with a scope of access (resource scope) to specify which mailboxes an app can access. This feature extends the current [RBAC](/exchange/permissions-exo/permissions-exo) model in Exchange Online and it replaces the need for Application Access Policies. Learn more [Role Based Access Control for Applications in Exchange Online | Microsoft Learn](/exchange/permissions-exo/application-rbac)

The Application Token now authorizes access directly through the mailbox permission. [Authenticate an IMAP, POP or SMTP connection using OAuth | Microsoft Learn](/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth) explains how Application Tokens work for SMTP.

### Enablement Steps

RBAC does not require mailbox permissions. To grant mailbox access to an Application Token for a set of users, the Exchange Admin needs to create a Management Role. Follow these steps to grant permission to the Application Token using RBAC.

**Setup Application**

- [Register your application](https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth#register-your-application)
- Refrain from adding any permissions to your application, as this process does not require any claims. Including the SMTP.SendAsApp claim would trigger an unnecessary check for mailbox permissions.


**Setup RBAC Policy**
- Create a service principal for the Azure Application. This creates a link between the Azure Application and the Exchange Service Principal.

  ```
  New-ServicePrincipal -AppId {Client Application ID in AAD} -ObjectId {Service principal object ID in AAD} -DisplayName {name}
  ```- Create a Security or Distribution Group and add to the group all the mailboxes that require access. You can use other recipient filter properties to grant access. This example shows only DG.
[New-DistributionGroup (ExchangePowerShell) | Microsoft Learn](/powershell/module/exchange/new-distributiongroup?view=exchange-ps)

- Create Management Scope

  ```
   New-ManagementScope -Name "RBAC Scope" -RecipientRestrictionFilter "MemberOfGroup -eq 'CN=rbac,OU={tenant name}.onmicrosoft.com,DC=COM'"
  ```
    [New-ManagementRole (ExchangePowerShell) | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/module/exchangepowershell/new-managementrole?view=exchange-ps)

- Create a Management Role: We support only the SMTP.SendAsApp role, so please ensure to pass it in the role.

  ```
  New-ManagementRoleAssignment -Name RBAC -Role 'Application SMTP.SendAsApp' -App {App ID} -CustomResourceScope 'RBAC Scope'
  ```
     [New-ManagementRoleAssignment (ExchangePowerShell) | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/module/exchangepowershell/new-managementroleassignment?view=exchange-ps)

**Get Access Token**
- [Get an access token](/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth). Make sure that you use https://outlook.office365.com/.default for the scope.

- Use this access token with XOAUTH2 command.








