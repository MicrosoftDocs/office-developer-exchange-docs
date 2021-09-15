---
title: "Web service API feature availability in Exchange and the EWS Managed API"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: "Learn about which EWS and web service API features are available in each version of Exchange and the EWS Managed API."
---

# Web service API feature availability in Exchange and the EWS Managed API

Learn about which EWS and web service API features are available in each version of Exchange and the EWS Managed API.
  
Exchange client applications often target many versions of Exchange. For this reason, you might want to design your application such that you can turn [EWS client features](ews-client-design-overview-for-exchange.md#EWSFeatures) on and off based on the version of Exchange that hosts your users' mailbox. This article provides information about which service API features are available in different versions of Exchange and the EWS Managed API. Use this information to design your application to apply broadly to customers running multiple versions of Exchange. 
  
For detailed information about the differences between versions of Exchange, review the EWS schema files and the associated [reference documentation](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx).
  
## API features by Exchange version
<a name="bk_apifeatures"> </a>

The Exchange web service APIs, including EWS and Autodiscover, are developed with multi-version compatibility in mind. Therefore, an application that targets Exchange 2007 also works against versions of Exchange starting with Exchange 2013, including Exchange Online and Exchange Online as part of Office 365. 
  
The following table indicates which API features are available in each version of Exchange and versions of the EWS Managed API starting with version 2.0. Because your application might target multiple versions of Exchange, it will be helpful for you to know which versions support the features that your client implements. You can use the Autodiscover service to discover which version of Exchange a client targets for a user so that you can turn features on and off depending on whether they are available to your users.
  
**Table 1. Web service feature availability in versions of Exchange and the EWS Managed API**

|API feature|Exchange Online (Office 365)|EWS Managed API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Ambiguous name resolution  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Apps for Outlook management  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Archive mailbox access](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Autodiscover (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Autodiscover (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Automatic replies (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Availability  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Availability (Rooms)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Bulk transfer  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Contact groups  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Conversation management  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime precision  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Delegate management  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Distribution list expansion  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Dumpster access](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[eDiscovery](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Enhanced time zones  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Folder permissions  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Identifier conversion](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Inbox management](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Item and folder access](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mailbox events (pull and push)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mailbox events (streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Mailtips  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Password expiration  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Personas](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Post items  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Public folder access](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Retention policies  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Search (indexed)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Search (store)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Synchronization](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Unified Contact Store](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Unified Messaging Web Service](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Unified Messaging (EWS-based)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[User configuration objects](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[User photos](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
You can find more information about the web service features that are available in different versions of Exchange by reading about the [EWS operations](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx), the [Autodiscover service](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx), and the [ExchangeService methods](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx).
  
## To learn more
<a name="bk_apifeatures"> </a>

If you want to go deeper to understand the specific differences between Exchange versions, you can do any of the following:
  
- Explore the [EWS schema](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) to investigate the differences between each version of EWS in more detail. 
    
- Download [EWSEditor](http://ewseditor.codeplex.com/). You can use EWSEditor to specify different target schema versions and submit queries based on the target schema version.
    
## See also

- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)   
- [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md) 
- [What's new in EWS and other web services in Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

