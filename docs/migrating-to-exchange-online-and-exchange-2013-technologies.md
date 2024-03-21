---
title: "Migrating to Exchange technologies"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: "If you're migrating from an earlier version of Exchange, use the information in this article to find out which development technologies are supported in current product versions, and which technology to migrate to."
ms.service: exchange
---

# Migrating to Exchange technologies

If you're migrating from an earlier version of Exchange, use the information in this article to find out which development technologies are supported in current product versions, and which technology to migrate to.
  
## Determine if your technology is available in current versions

Use the following table to determine whether a development technology is supported in Exchange Online or Exchange 2019. If the technology is not supported, see [Choose a development technology to migrate to](#bk_choose).

<br/> 

**Exchange development technologies and product versions**

|Technology|Office 365 and Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Office 365 APIs platform overview](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X²  <br/> |X¹ ²  <br/> ||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Web Services (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mail apps for Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Outlook Object Model (OOM)](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Management Shell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Backup and restore](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Transport agents](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Active Directory Services Interface (ADSI)  <br/> ||||||X  <br/> |
|Collaborative Data Objects for Exchange (CDOEX)  <br/> ||||||X  <br/> |
|Collaborative Data Objects for Windows 2000 (CDOSYS)  <br/> ||||||X  <br/> |
|Exchange OLE DB Provider (EXOLEDB)  <br/> ||||||X  <br/> |
|Exchange Store Event Sinks  <br/> ||||||X  <br/> |
|Incremental Change Synchronization (ICS)  <br/> ||||||X  <br/> |
|Lightweight Directory Access Protocol (LDAP)  <br/> ||||||X  <br/> |
|[Messaging API (MAPI)](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App customization  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Web Distributed Authoring and Versioning (WebDAV)  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

¹REST API and Graph API require the Cumulative Update 3 for Exchange 2016.

²Only hybrid customers are able to take advantage of the REST APIs for both Office 365 and on-premises mailboxes.

## Choose a development technology to migrate to

If the technology your application uses is not supported or deemphasized in Exchange Online or Exchange 2013, use the following table to decide which technology to migrate to.
  
**Recommended technology migration paths**

|**Technology**|**Supported in Office 365, Exchange Online, and Exchange 2019?**|**Migrate to**|**More info**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Yes, but deemphasized <br/>|[Exchange Management Shell](management/exchange-management-shell.md)<br/> |None.  <br/> |
|CDOEX  <br/> |No  <br/> |[EWS Managed API or EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |The EWS Managed API and EWS can access the same Exchange store that CDOEX provides. Unlike client applications built by using CDOEX, you can run EWS applications on a local or remote computer.  <br/> |
|CDOEXM  <br/> |No <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Exchange Management Shell commands control Exchange servers, storage groups, databases, and users more simply than the corresponding CDOEXM APIs. Plus, you can easily migrate your CDOEXM applications to Exchange Management Shell commands.  <br/> |
|CDOSYS<br/> |No<br/> |[Transport agents](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Use transport agents for notification-based applications that work with versions of Exchange starting with Exchange 2010.<br/><br/> CDOSYS is included in current versions of Windows. The functionality in CDOSYS is available in the .NET Framework.  <br/> |
|CDOWF  <br/> |No  <br/> |[Windows Workflow Foundation (WWF)](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |You can use WWF to create advanced workflow applications that work with Exchange 2007.   <br/> |
|ExOLEDB  <br/> |No  <br/> |[EWS Managed API or EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |The EWS Managed API and EWS provide the same access to the Exchange store that ExOLEDB provides. Unlike client applications built by using ExOLEDB, You can run EWS applications on a local or remote computer.  <br/> |
|ICS  <br/> |Yes, but deemphasized  <br/> |EWS Managed API or EWS<br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) and [synchronize mailbox data](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).  <br/> |
|LDAP  <br/> |Yes, but deemphasized  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |None.  <br/> |
|MAPI  <br/> |Yes, but deemphasized  <br/> |Office 365 APIs platform overview, EWS Managed API, EWS <br/> |Although MAPI is currently a supported development technology, you will eventually have to redesign your MAPI applications to use a newer technology.<br/><br/>If your MAPI application is performing simple read, write, and update operations on mail, calendar, or contact objects, and targets Office 365, Exchange 2019² or Exchange 2016¹ ² you can use the [Office 365 REST APIs for mail, calendars, and contacts](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>If you are targeting Exchange on-premises and you need to access all the properties that MAPI can access, you can use the EWS Managed API or EWS and either [schematized properties or extended properties](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx).<br/><br/>**NOTE**: The [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) class provides access to MAPI from the EWS Managed API, and the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element provides access to MAPI properties from EWS.           |
|Outlook Web App customization  <br/> |No  <br/> |[Mail apps](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |None.  <br/> |
|Store event sinks  <br/> |No  <br/> |EWS Managed API or EWS <br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) and [synchronize mailbox data](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).<br/><br/>The notifications in EWS provide the same access to the Exchange store that store event sinks provide. You can use Visual Studio tools to streamline the development of store event-aware client applications that use EWS.  <br/> |
|Streaming backup and restore  <br/> |No  <br/> |[Volume Shadow Copy Service (VSS) writer](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |None.  <br/> |
|WebDAV  <br/> |No  <br/> |Office 365 APIs platform overview, EWS Managed API or EWS <br/> |If your WebDAV application is performing simple read, write, and update operations on mail, calendar, or contact objects, and you will be targeting Office 365, Exchange 2019² or Exchange 2016¹ ² you can use the [Office 365 REST APIs for mail, calendars, and contacts](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>Otherwise, if you are targeting Exchange on-premises and you need access to the same properties in the Exchange store that WebDAV provides, use the EWS Managed API or EWS.  <br/> |
|WebDAV notifications  <br/> |No  <br/> |EWS Managed API or EWS<br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md).  <br/> |
|Web forms  <br/> |No  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Switch to ASP.NET and update applications to access mailbox and server information by using EWS.  <br/> |
|WMI providers  <br/> |No  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |None.  <br/> |
   
¹REST API and Graph API require the Cumulative Update 3 for Exchange 2016.

²Only hybrid customers are able to take advantage of the REST APIs for both Office 365 and on-premises mailboxes.

## See also

- [Selecting an API or technology for developing solutions for Outlook](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [On-Premises Architectural Requirements for the REST API](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
