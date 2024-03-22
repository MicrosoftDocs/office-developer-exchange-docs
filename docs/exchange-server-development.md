---
title: "Exchange Online and Exchange development"
manager: sethgros
ms.date: 01/22/2022
ms.audience: Developer
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: "Find in-depth developer documentation for Exchange Server, including Exchange Online as part of Office 365 and Exchange Server on-premises versions."
localization_priority: Priority
ms.service: exchange
---

# Exchange Online and Exchange development

Find in-depth developer documentation for Exchange Server, including Exchange Online as part of Office 365 and Exchange Server on-premises versions.

You can use the how to, get started, new feature, and API reference documentation to develop tools to access and manage mailbox data from services, websites, desktop computers, and mobile devices, and to create custom solutions for email, calendar, contacts, and other items that are stored in Exchange Online or on an Exchange 2010, 2013, 2016, and 2019 server.

You can use Graph API, REST API, Exchange Web Services (EWS), Autodiscover, Outlook add-ins, or other APIs to develop your applications. This page helps you choose the right Exchange technology.

> [!NOTE]
> We’re removing the ability to use Basic authentication in Exchange Online for EWS beginning October 2022. For more information, see [Deprecation of Basic authentication in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). You should use OAuth authentication instead. [Authenticate an EWS application by using OAuth](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth) and [Authenticate an IMAP, POP or SMTP connection using OAuth](/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth).

## Exchange developer content

Use the following table to identify the technology and related API content that will help you meet your development goals.

> [!IMPORTANT]
> Microsoft Graph is the recommended API to use for accessing Exchange Online data. New applications designed to access Exchange Online data should use Microsoft Graph.

|If you are building...|Start here|
|:-----|:-----|
|A REST-based app to access Exchange Online as part of Office 365|[Microsoft Graph REST APIs for mail, calendars, and contacts](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|A context-sensitive app to display information in Outlook, Outlook Web App, or OWA for Devices |[Outlook add-ins and EWS in Exchange](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|A mailbox client that is not based on the .NET Framework or Java |[Explore the EWS Managed API, EWS, and web services in Exchange](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|A mailbox client that uses the .NET Framework to access EWS |[Get started with EWS Managed API client applications](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|A mailbox client that uses Java to access EWS |[EWS Java API on GitHub](https://github.com/OfficeDev/ews-java-api) |
|An application that customizes the Outlook user interface or relies on Outlook business logic  |[Outlook VBA reference](https://msdn.microsoft.com/VBA/VBA-Outlook) |
|An application that targets Exchange Online or Exchange 2013 that you need to migrate from a previous version of Exchange  |[Migrating to Exchange technologies](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|A custom management tool that uses Windows PowerShell from managed code   |[Exchange Management Shell](management/exchange-management-shell.md) |
|A solution to back up or restore Exchange data  |[Backup and restore for Exchange](backup-restore/backup-and-restore-for-exchange-2013.md) |
|An extension to support accessing messages in the transport pipeline   |[Transport agents in Exchange](transport-agents/transport-agents-in-exchange-2013.md)  |
|A mailbox client for a mobile device   |[Exchange ActiveSync](https://technet.microsoft.com/library/aa998357.aspx) |

## Exchange interactions with custom applications

Some of these technologies enable your applications to work with data that is stored in Exchange, and others are used to manage and control the Exchange server. In many cases, you can use more than one programming technology or language to accomplish a task, which makes it possible for you to use the technologies and languages that you are familiar with. For example, you can set properties on items in the Exchange store by using the Mail REST API, EWS, or the EWS Managed API.

Exchange interacts with custom applications in a variety of ways, depending on the application architecture and functionality. At its core, Exchange not only transports messages, but also maintains mailboxes, executes form-based applications, and more.

|Exchange interaction|Description|
|:-----|:-----|
|**Message transport**|Exchange serves as a standard mail server for applications that send messages.<br/>Exchange includes several APIs that transfer messages, including REST, EWS, and the EWS Managed API.<br/>In addition, applications can use transport agents to respond as messages are processed and delivered by Exchange. |
|**Mailbox storage** |Exchange provides a hierarchical structure of folders, items, and properties for applications that access data stored in mailboxes.<br/>You can access that stored information by using a combination of database and component object styles.<br/>You can perform queries on the data, and Exchange manages access to the stored data based on user and store permissions.<br/>Applications that handle mailbox data typically use REST, EWS, or the EWS Managed API.|
|**Managed enterprise server** |Exchange functions as a managed server for applications that manage Exchange servers and stores.<br/>Applications can configure, control, and monitor current activity and the health of Exchange servers across the organization.<br/>Exchange management applications use the Exchange Management Shell to manage Exchange servers. |

## See also

- [Server API reference for Exchange](https://msdn.microsoft.com/library/dn186243(v=exchg.150).aspx)
- [Read about Exchange on Office Blogs](https://www.microsoft.com/microsoft-365/blog/)
- [Get 101 code samples for Exchange 2013](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [Get the EWS Managed API (GitHub)](https://github.com/OfficeDev/ews-managed-api/blob/main/README.md)
- [Get support for Exchange Server](https://support.microsoft.com/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)
