---
title: "Exchange Online and Exchange 2013 development"

manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer


localization_priority: Normal
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: "Create custom solutions for email, calendar, contacts, and other items that are stored in Exchange Online or on an Exchange 2013 server. You can use Exchange Web Services (EWS), Autodiscover, mail apps for Office, or other APIs to develop your applications."
---

# Exchange Online and Exchange 2013 development

Create custom solutions for email, calendar, contacts, and other items that are stored in Exchange Online or on an Exchange 2013 server. You can use Exchange Web Services (EWS), Autodiscover, mail apps for Office, or other APIs to develop your applications. 
  
## Explore the Exchange Online and Exchange 2013 developer content

Use the following table to identify the technology and related API content that will help you meet your development goals. 
  
|**If you are building…**|**Start here**|
|:-----|:-----|
|A REST-based app to access Exchange Online as part of Office 365.  <br/> |[Office 365 REST APIs for mail, calendars, and contacts](http://msdn.microsoft.com/library/3b2e71a6-5fa5-4008-b243-d3a6e9173b3d%28Office.15%29.aspx) <br/> |
|A context-sensitive app to display information in Outlook, Outlook Web App, or OWA for Devices.  <br/> |[Mail apps for Outlook and EWS in Exchange](http://msdn.microsoft.com/library/821c8eb9-bb58-42e8-9a3a-61ca635cba59%28Office.15%29.aspx) <br/> |
|A mailbox client that is not based on the .NET Framework or Java.  <br/> |[Explore the EWS Managed API, EWS, and web services in Exchange](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |
|A mailbox client that uses the .NET Framework to access EWS.  <br/> |[Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx) <br/> |
|A mailbox client that uses Java to access EWS.  <br/> |[EWS Java API on GitHub](https://github.com/OfficeDev/ews-java-api) <br/> |
|An application that customizes the Outlook user interface or relies on Outlook business logic.  <br/> |[Outlook 2013 developer reference](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |
|An application that targets Exchange Online or Exchange 2013 and you need to migrate from a previous version of Exchange.  <br/> |[Migrating to Exchange Online and Exchange 2013 technologies](http://msdn.microsoft.com/library/946a722f-0892-4a59-9e58-a291bfb6834a%28Office.15%29.aspx) <br/> |
|A custom management tool that uses Windows PowerShell from managed code.  <br/> |[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |
|A solution to back up or restore Exchange data.  <br/> |[Backup and restore for Exchange 2013](http://msdn.microsoft.com/library/329902d9-0ecb-4cfb-86dd-5ce863deff3f%28Office.15%29.aspx) <br/> |
|An extension to support accessing messages in the transport pipeline.  <br/> |[Transport agents in Exchange 2013](http://msdn.microsoft.com/library/36d63aa6-1b72-4670-b5c3-da685f3017cb%28Office.15%29.aspx) <br/> |
|A mailbox client for a mobile device.  <br/> |[Exchange ActiveSync](http://technet.microsoft.com/en-us/library/aa998357.aspx) <br/> |
   
Some of these technologies enable your applications to work with data that is stored in Exchange, and others are used to manage and control the Exchange server. In many cases, you can use more than one programming technology or language to accomplish a task, which makes it possible for you to use the technologies and languages that you are familiar with. For example, you can set properties on items in the Exchange store by using the Mail REST API, EWS, or the EWS Managed API.
  
Exchange interacts with custom applications in a variety of ways, depending on the application architecture and functionality. At its core, Exchange not only transports messages, but also maintains mailboxes, executes form-based applications, and more.
  
****

|**Exchange interaction**|**Description**|
|:-----|:-----|
|Message transport  <br/> |Exchange serves as a standard mail server for applications that send messages. Exchange includes several APIs that transfer messages, including REST, EWS, and the EWS Managed API. In addition, applications can use transport agents to respond as messages are processed and delivered by Exchange.  <br/> |
|Mailbox storage  <br/> |Exchange provides a hierarchical structure of folders, items, and properties for applications that access data stored in mailboxes. You can access that stored information by using a combination of database and component object styles. You can perform queries on the data, and Exchange manages access to the stored data based on user and store permissions. Applications that handle mailbox data typically use REST, EWS, or the EWS Managed API.  <br/> |
|Managed enterprise server  <br/> |Exchange functions as a managed server for applications that manage Exchange servers and stores. Applications can configure, control, and monitor current activity and the health of Exchange servers across the organization. Exchange management applications use the Exchange Management Shell to manage Exchange servers.  <br/> |
   

