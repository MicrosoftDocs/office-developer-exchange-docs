---
title: "Configuration options for EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: "Find information about configuration settings that your EWS client can access, and the configurable Exchange settings that can affect your EWS client."
---

# Configuration options for EWS in Exchange

Find information about configuration settings that your EWS client can access, and the configurable Exchange settings that can affect your EWS client. 
  
Many configuration settings can affect what your EWS client application can do. These configuration settings are either: 
  
- Read-only or read-writeable from the client.
    
- Accessed on the Exchange server that hosts your EWS service.
    
A client can access settings on Exchange Online, Exchange Online as part of Office 365, and an on-premise Exchange server. All on-premise Exchange server settings are available to Exchange administrators; however, not all of these settings are available to Exchange Online tenant administrators. This article describes which configuration settings clients, Exchange Server administrators, and Exchange Online tenant administrators can access.
  
## Configuration settings that clients can access

Your client application can get and set a number of configuration options from the Exchange server. Configuration settings that all EWS applications need are provided by the Autodiscover service. Other configuration settings are used for specific application scenarios. 
  
**Table 1. Web service features that provide configuration options for EWS clients**

|**Feature**|**Description**|
|:-----|:-----|
|Autodiscover service  <br/> |The [Autodiscover service](autodiscover-for-exchange.md) provides your client applications with configuration information so that your client can automatically configure itself to communicate with EWS.  <br/> |
|Custom configuration information stored in a mailbox  <br/> |You can use one of several options to [store custom configuration information](persistent-application-settings-in-ews-in-exchange.md) in your mailbox: user configuration objects, custom items, or extended properties.  <br/> |
|Delegate management  <br/> | EWS provides CRUD operations for managing delegate access to a mailbox. Delegates are users who have been given permission to access another user's mailbox.<br/><br/>  You can use the [delegate management operations](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) to enable delegate management by using EWS, or, if you're using the EWS Managed API, you can use the following methods:<br/><br/>- [ExchangeService.AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|eDiscovery search configuration  <br/> |eDiscovery client applications can get [search configuration information](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) that includes an eDiscovery search query, a list of searchable mailboxes, and the identifier of in-place mailbox holds.  <br/> |
|Folder permissions  <br/> |Folder permissions limit what a user can do in a public folder, and in the case of delegate access, what a delegate can do in another user's folder. You can use either the [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method or the [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to access the permission set of every folder, including public folders, shared private folders, or folders to which users have delegate access.  <br/> |
|Mail tips, Unified Messaging, or protection rules  <br/> |The [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) provides read-only [service configuration information](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) for mail tips, Unified Messaging, and protection rules.  <br/> |
   
## Configuration settings that administrators can access on the Exchange server

Most client application scenarios don't require changes to server configuration settings; however, some scenarios do. For example, to enable a middle-tier application to act as a user, you need to set Exchange Impersonation on the server. Note that some settings can only be accessed on on-premise Exchange servers. If you are targeting Exchange Online, your client application might need to work with the default settings.
  
**Table 2. Exchange server configuration options that affect EWS clients**

|**Feature**|**Accessible from Exchange Online?**|**For more information, see…**|
|:-----|:-----|:-----|
|Virtual directory settings (including authentication)  <br/> |No  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|Autodiscover  <br/> |No  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Compliance  <br/> |Yes  <br/> |[Archiving](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [eDiscovery](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [Retention hold](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [Data loss prevention](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Delegate management  <br/> |Yes  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange Impersonation  <br/> |Yes  <br/> |[Configure Exchange Impersonation](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|Mail tips, Unified Messaging, or protection rules  <br/> |Yes  <br/> |[MailTips](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [Unified Messaging Cmdlets](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook Protection Rules](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Throttling  <br/> |No  <br/> |[Throttling settings](ews-throttling-in-exchange.md) <br/> |
|User agent filtering  <br/> |Yes  <br/> |[User agent filtering](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## See also

- [Get service configuration information by using EWS in Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)   
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)   
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    

