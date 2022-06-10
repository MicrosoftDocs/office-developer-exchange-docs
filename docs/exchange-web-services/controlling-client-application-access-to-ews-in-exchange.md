---
title: "Controlling client application access to EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: "Learn about the options for managing client application access to EWS."
localization_priority: Priority
---

# Controlling client application access to EWS in Exchange

Learn about the options for managing client application access to EWS.
  
Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations. Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications. Access control for EWS is based on domain accounts. When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect. 
  
## Access control for EWS clients and users
<a name="bk_configure"> </a>

Your test or production server administrator can configure access control for clients that connect to EWS in the following ways: 
  
- By blocking all client applications from connecting.
    
- By allowing specific client applications only to connect.
    
- By allowing any client application to connect except those that are specifically blocked.
    
- By allowing any client application to connect.
    
Applications are identified by the user agent string that they send in the HTTP web request.
  
> [!IMPORTANT]
> Application-level blocking is not a security feature. The user agent string is easily spoofed. If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS. 
  
Administrators can also configure access control for mailbox owners that connect to EWS in the following ways: 
  
- By blocking or allowing an entire organization.
    
- By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.
    
- By blocking or allowing an individual mailbox owner.
    
Specific access control settings override general access control settings. For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed. 
  
## Delegation and EWS access management
<a name="bk_delegation"> </a>

When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access. If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access. 
  
## Impersonation and EWS access management
<a name="bk_impersonation"> </a>

Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner. For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are. Other applications, such as mail clients, do have to use the mailbox owner's EWS settings. 
  
Administrators should create an impersonation account for each application or application class that they use on their server. This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions. 
  
To enable impersonation accounts, your test or production server administrator should do one of the following: 
  
- Add the Authenticated Users group to the Pre-Win2K Compatible Access Group. 
    
- Add the Exchange Servers group to the Windows Authorization Access group. 
    
## Exchange Management Shell cmdlets for access management
<a name="bk_cmdlets"> </a>

Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls: 
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx)   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx)   
- [Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx)   
- [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx)
    
## See also

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)  
- [Control access to EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)
- [Exchange Server PowerShell (Exchange Management Shell)](/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
