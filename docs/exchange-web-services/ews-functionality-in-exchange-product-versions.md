---
title: "EWS functionality in Exchange product versions"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
 
 
localization_priority: Normal
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: "EWS implements new functionality in new product releases. Use the information in this article to determine whether the version of Exchange you're targeting includes support for the data or features you need access to."
---

# EWS functionality in Exchange product versions

EWS implements new functionality in new product releases. Use the information in this article to determine whether the version of Exchange you're targeting includes support for the data or features you need access to. 
  
The following table lists the versions of Exchange that include EWS and the major features that were introduced in each version.
  
## EWS features by product version

|**Product version**|**Features**|
|:-----|:-----|
|Office 365 and Exchange Online  <br/> |Includes all the features in the current version of Exchange in addition to any new features that are added for online clients.  <br/> |
|Exchange 2013 SP1  <br/> | Includes all features introduced in Exchange 2013. The following features were introduced in Exchange 2013 SP1:  <br/>  Read receipts can now be suspended for updates and deletions.  <br/>  You can get [moderated transport](http://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) approval information.  <br/>  Voting responses can be viewed.  <br/>  The [SetHoldOnMailboxes](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) method and [SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) operation accept all the parameters in a single object.  <br/>  eDiscovery searches can specify a language for search queries and a culture-specific format for date ranges.  <br/>  The [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object can now access the [StreamingSubscription](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) objects.  <br/>  Conversations have a setting to indicate whether they contain email messages that are protected by IRM.  <br/>  Meeting attendees can propose new start and end times for meetings and include them in their meeting response.  <br/>  The SOAP Autodiscover [GetUserSettings](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) method now returns the [GroupingInformation](http://msdn.microsoft.com/EN-US/library/office/dn529149%28v=exchg.150%29.aspx) setting that is used maintain affinity for a multiple mailbox event subscription.  <br/> |
|Exchange 2013  <br/> | Includes all features introduced in Exchange 2010 SP2. The following features were introduced in Exchange 2013:  <br/>  Archiving  <br/>  eDiscovery  <br/>  Personas  <br/>  Retention policies  <br/>  Unified Contact Store  <br/>  User photos  <br/> |
|Exchange 2010 SP2  <br/> | Includes all the features introduced in Exchange 2010 SP1. The following features were introduced in Exchange 2010 SP2:  <br/>  Get Password Expiration  <br/>  DateTime precision  <br/>  Updated property identifiers for contacts  <br/>  New impersonation scenarios  <br/> |
|Exchange 2010 SP1  <br/> | Includes all the features introduced in Exchange 2010. The following features were introduced in Exchange 2010 SP1:  <br/>  Create, retrieve and modify Inbox rules  <br/>  Programmatic access to Archive Mailbox  <br/>  Conversations actions  <br/>  Firewall traversing notifications  <br/>  Improved administration features  <br/>  Improved mixed version support  <br/>  Throttling protection support  <br/>  Control of application access to EWS  <br/>  Client certificate authentication support  <br/> |
|Exchange 2010  <br/> | Includes all features introduced in Exchange 2007 SP1. The following features were introduced in the initial release version of Exchange 2010:  <br/>  Full Private Distribution List  <br/>  User Configuration Objects  <br/>  Folder Associated Items  <br/>  Message tracking  <br/>  Unified Messaging  <br/>  SOAP Autodiscover  <br/>  Enhanced Time Zone support  <br/>  Room resource availability information  <br/>  Indexed search  <br/>  Dumpster access  <br/>  MailTips information  <br/> |
|Exchange 2007 SP1  <br/> | Includes all the features introduced in Exchange 2007. The following features were introduced in Exchange 2007 SP1:  <br/>  Delegate management  <br/>  Folder permissions  <br/>  Public folders  <br/>  Post items  <br/>  ID conversion  <br/> |
|Exchange 2007  <br/> | The following features were introduced in the initial release version of Exchange 2007:  <br/>  Full access to items, folders, and attachments (Create, Get, Update, Delete)  <br/>  Availability  <br/>  Out of Office settings  <br/>  Notifications  <br/>  Synchronization  <br/>  Name resolution  <br/>  Distribution list (DL) expansion  <br/>  Search  <br/> |
   
## See also

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [Migrating to Exchange technologies](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

