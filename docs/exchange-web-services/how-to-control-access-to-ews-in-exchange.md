---
title: "Control access to EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: "Find out how to control access to EWS for users, applications, or the entire organization."
localization_priority: Priority
---

# Control access to EWS in Exchange

Find out how to control access to EWS for users, applications, or the entire organization.
  
Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS). If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.
  
## Exchange Management Shell cmdlets for configuring access control
<a name="bk_Cmdlets"> </a>

You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx) - Sets parameters for a particular mailbox.    
- [Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx) - Shows you the parameters for the entire organization.    
- [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx) - Sets the parameters for the entire organization. 

<a name="bk_Examples"> </a>

## Examples: Controlling access to EWS

Let's take a look at a few scenarios that show you how you can control access to your application.
  
**Table 1. Commands for controlling access to EWS**

|If you want to |Use this command|
|:-----|:-----|
|Block all client applications from using EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>This allows applications listed in the AllowList to connect. In this example, no applications are included in the AllowList, so no applications can use EWS. |
|Allow a list of client applications to use EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>This allows specific applications to use EWS. In this example, any application that has a user agent string that starts with "OWA/" is allowed access. |
|Allow all client applications to use EWS except those that are specifically blocked. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>This example only blocks applications from using EWS that have a user agent string that starts with "OWA/". |
|Allow all client applications to use EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> Because no BlockList is specified, all applications can use EWS. |
|Block the entire organization from using EWS. | `Set-OrganizationConfig -EwsEnabled:$false` |
|Allow the entire organization to use EWS. | `Set-OrganizationConfig -EwsEnabled:$true`|
|Block an individual mailbox from using EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|Allow an individual mailbox to use EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## See also

- [Setting up your EWS application](setting-up-your-ews-application.md)    
- [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server PowerShell (Exchange Management Shell)](/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
