---
title: "Start using web services in Exchange"
 
 
manager: sethgros
ms.date: 2/26/2019
ms.audience: Developer
 
 
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: "Find information to help you get started with EWS and other web services in Exchange."
localization_priority: Priority
---

# Start using web services in Exchange

Find information to help you get started with EWS and other web services in Exchange.
  
The [web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) provide access to mailbox data stored in Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2007, and enable you to create custom applications that you can use to manage that information according to the requirements of your organization. While the range of EWS and web service applications that you can create is practically infinite, certain fundamental concepts apply for any type of application. This section provides information about the fundamental concepts you need to be familiar with in order to start using EWS and other web services in Exchange. 
  
## Build your knowledge
<a name="bk_Knowledge"> </a>

Whether you use the .NET Framework or another platform to develop your web service application, you will want to understand some important concepts before you begin your development project. 
  
**Table 1. Web services concepts**

|**Concept**|**Summary**|
|:-----|:-----|
|[Architecture](ews-applications-and-the-exchange-architecture.md) <br/> |Learn about how EWS works within the Exchange architecture and the protocols it uses.  <br/> |
|[EWS application types](ews-application-types.md) <br/> |Find out about the most common types of applications that you can create by using EWS in Exchange.  <br/> |
|[EWS access](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Exchange administrators can limit access to EWS globally for the entire organization, for individual users, and to individual applications. Find out which access level is right for you.  <br/> |
|[Setup](setting-up-your-ews-application.md) <br/> |Find information about the tasks you need to complete in order to create applications that use the EWS Managed API or EWS to communicate with Exchange.  <br/> |
|[Authentication](authentication-and-ews-in-exchange.md) <br/> |Learn about the authentication options for connecting to Exchange Online and Exchange on-premises.  <br/> |
|[Autodiscover](autodiscover-for-exchange.md) <br/> |Learn about the set of services that you can use to discover the URL endpoint where a user's account can access information via EWS.  <br/> |
|[Mailbox server](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx) <br/> |Find out about the primary repository of information made available to an EWS client. EWS has access to a limited set of information stored in Active Directory Domain Services (AD DS).  <br/> |
|[Mail apps for Outlook and EWS](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Find information about mail apps for Outlook and how they work with EWS in Exchange.  <br/> |
|[Office 365 REST APIs for mail, calendars, and contacts](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |Learn about the Office 365 APIs that you can use to access mail, calendars, and contacts in Exchange Online as part of Office 365.  <br/> |
|[The EWS Managed API](get-started-with-ews-managed-api-client-applications.md) <br/> |Find information about the preferred client API for .NET Framework developers.  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |Find information about creating your first application by using EWS XML requests and responses.  <br/> |
|[EWS functionality in Exchange product versions](ews-functionality-in-exchange-product-versions.md) <br/> |Find out what EWS functionality is available in version of Exchange.  <br/> |
|[Trace and troubleshoot](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |Find out how to trace EWS requests and responses in order to troubleshoot errors in your EWS Managed API application.  <br/> |
   
## Create your first application
<a name="create"> </a>

If you're ready to get to the business of writing your first .NET Framework or EWS client application, see [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md) or [Get started with EWS client applications](get-started-with-ews-client-applications.md).
  
## Get code samples
<a name="samples"> </a>

To find code samples and examples that show you how to work with EWS and other web services in Exchange, see the following resources:
  
- [Exchange code samples](https://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Exchange API documentation](develop-web-service-clients-for-exchange.md)
    
- [Exchange Development forum](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)
    
Many other samples are available in blogs, code demonstration sites, and forums. We also recommend that you download the [EWSEditor](http://ewseditor.codeplex.com/). This project implements most of the EWS functionality; you can find examples of all the core EWS functionality here.
  
If you're not a .NET Framework developer, you can find many client libraries out there for EWS development that use Java, Python, PHP, and other languages. 
  
## Ask questions and solve problems
<a name="questions"> </a>

Need help getting things done and you're not finding answers? You can search the [Exchange Development forum](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) to find out whether someone else has encountered and resolved the same issue. A community of contributors have answered hundreds of questions about Exchange development. You can also find third-party sites, forums, and blogs that cover Exchange development and might have the solution you're looking for. 
  
Contact [Microsoft support](https://support.microsoft.com/) if you need additional assistance. The Exchange Developer support team is staffed with seasoned professionals who can help answer your questions about Exchange development. 
  
## See also

- [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md) 
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md) 
- [Web services reference for Exchange](../web-service-reference/web-services-reference-for-exchange.md)
    

