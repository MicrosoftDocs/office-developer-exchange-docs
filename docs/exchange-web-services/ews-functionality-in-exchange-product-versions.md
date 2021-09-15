---
title: "EWS functionality in Exchange product versions"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: "EWS implements new functionality in new product releases. Use the information in this article to determine whether the version of Exchange you're targeting includes support for the data or features you need access to."
---

# EWS functionality in Exchange product versions

EWS implements new functionality in new product releases. Use the information in this article to determine whether the version of Exchange you're targeting includes support for the data or features you need access to. 
  
The following table lists the versions of Exchange that include EWS and the major features that were introduced in each version.
  
## EWS features by product version

|**Product version**|**Features**|
|:-----|:-----|
|Office 365 and Exchange Online |Includes all the features in the current version of Exchange in addition to any new features that are added for online clients.  |
|Exchange 2013 SP1 | Includes all features introduced in Exchange 2013. The following features were introduced in Exchange 2013 SP1:<ul><li>Read receipts can now be suspended for updates and deletions.</li><li>You can get [moderated transport](https://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) approval information.</li><li>Voting responses can be viewed.</li><li>The [SetHoldOnMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) method and [SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) operation accept all the parameters in a single object.</li><li>eDiscovery searches can specify a language for search queries and a culture-specific format for date ranges.</li><li>The [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object can now access the [StreamingSubscription](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) objects.</li><li>Conversations have a setting to indicate whether they contain email messages that are protected by IRM.</li><li>Meeting attendees can propose new start and end times for meetings and include them in their meeting response.</li><li>The SOAP Autodiscover [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) method now returns the [GroupingInformation](https://msdn.microsoft.com/library/office/dn529149%28v=exchg.150%29.aspx) setting that is used maintain affinity for a multiple mailbox event subscription.</li></ul> |
|Exchange 2013  | Includes all features introduced in Exchange 2010 SP2. The following features were introduced in Exchange 2013:  <ul><li>  Archiving</li><li>eDiscovery</li><li>Personas</li><li>Retention policies</li><li>Unified Contact Store</li><li>User photos</li></ul> |
|Exchange 2010 SP2  | Includes all the features introduced in Exchange 2010 SP1. The following features were introduced in Exchange 2010 SP2:  <ul><li>  Get Password Expiration</li><li>DateTime precision</li><li>Updated property identifiers for contacts</li><li>New impersonation scenarios</li></ul> |
|Exchange 2010 SP1  | Includes all the features introduced in Exchange 2010. The following features were introduced in Exchange 2010 SP1:  <ul><li>  Create, retrieve and modify Inbox rules</li><li>Programmatic access to Archive Mailbox</li><li>Conversations actions</li><li>Firewall traversing notifications</li><li>Improved administration features</li><li>Improved mixed version support</li><li>Throttling protection support</li><li>Control of application access to EWS</li><li>Client certificate authentication support</li></ul> |
|Exchange 2010  | Includes all features introduced in Exchange 2007 SP1. The following features were introduced in the initial release version of Exchange 2010: <ul> <li>  Full Private Distribution List</li><li>User Configuration Objects</li><li>Folder Associated Items</li><li>Message tracking</li><li>Unified Messaging</li><li>SOAP Autodiscover  </li><li>Enhanced Time Zone support</li><li>Room resource availability information</li><li>Indexed search</li><li>Dumpster access</li><li>MailTips information</li></ul> |
|Exchange 2007 SP1  | Includes all the features introduced in Exchange 2007. The following features were introduced in Exchange 2007 SP1:  <ul><li>  Delegate management</li><li>Folder permissions</li><li>Public folders</li><li>Post items</li><li>ID conversion</li></ul> |
|Exchange 2007  | The following features were introduced in the initial release version of Exchange 2007:  <ul><li>  Full access to items, folders, and attachments (Create, Get, Update, Delete)</li><li>Availability</li><li>Out of Office settings</li><li>Notifications</li><li>Synchronization</li><li>Name resolution</li><li>Distribution list (DL) expansion</li><li>Search</li></ul> |
   
## See also

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [Migrating to Exchange technologies](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

