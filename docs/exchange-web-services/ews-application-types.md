---
title: "EWS application types"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: "Find out about the most common types of applications that you can create by using EWS in Exchange."
localization_priority: Priority
---

# EWS application types

Find out about the most common types of applications that you can create by using EWS in Exchange.
  
The [EWS and Exchange architecture](ews-applications-and-the-exchange-architecture.md) provides a uniform development model that you can use to create the most common types of applications in a consistent way, including the following: 
  
- [Client applications](#bk_clientapps) — Standalone applications that use EWS to access Exchange data. Outlook and Outlook Web App are examples of client applications. 
    
- [Portal applications](#bk_portalapps) — Applications that extend an existing web page by including information retrieved from Exchange, such as free/busy or contact information. A SharePoint web part that retrieves Exchange data is an example of a portal application. 
    
- [Service applications](#bk_serviceapps) — Background jobs used to integrate or synchronize data from Exchange into an existing system. For example, an application that synchronizes contact information from Exchange into a CRM application. 
    
Each of these application models can use a common code base to retrieve information from Exchange - so you don't need to change the EWS code used to retrieve item information between a client, portal, or service application. What might change from one application to the next is the mailbox access and authentication mechanism. For example, client applications commonly use direct user access and basic or NTLM authentication, whereas a service application likely uses impersonation for mailbox access and OAuth authentication.
  
## Client applications
<a name="bk_clientapps"> </a>

An EWS client application is any standalone application that uses EWS to retrieve information from the Exchange store. EWS client applications use direct client access or delegate access to retrieve data from the mailbox store. The following are some examples of client applications that use EWS:
  
- Outlook, in features such as MailTips, availability, and user OOF status
    
- OWA for Devices
    
- Outlook for Mac 2011
    
- Lync, for availability information
    
Client applications commonly use direct access and basic or NTLM authentication, so that users are limited to accessing information in their own mailbox with their own logon credentials. Client applications should also support delegate access for users who have been given permission to access another user's mailbox.
  
## Portal applications
<a name="bk_portalapps"> </a>

A portal application extends an existing web page or portal to include Exchange mailbox information as a personalized component of the page. SharePoint web parts are the most common portal applications and provide users with a personalized experience by providing views into Exchange mailbox data, such as unread messages, most recent messages, and calendar events, alongside their commonly viewed SharePoint portal page. EWS portal applications can use direct client access, delegate access, or impersonation to retrieve data from the mailbox store. Because Exchange 2013 and SharePoint 2013 both support the OAuth authorization protocol for server-to-server authentication, OAuth provides the most seamless and secure authentication method.
  
## Service applications
<a name="bk_serviceapps"> </a>

A service application is usually a background job built into an existing application that extends to Exchange to correlate data between the system and the Exchange store. Service applications typically do not have a user interface and use impersonation or OAuth for authentication and access. Creating a service account to impersonate users is common in EWS service apps because you can grant a single account permission to impersonate a set of users and perform mailbox operations for those accounts. For example, an EWS service application can synchronize data between marketing lists in a CRM solution and Exchange distribution groups by using a service account and impersonation.
  
## See also


- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS applications and the Exchange architecture](ews-applications-and-the-exchange-architecture.md)
    
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
    

