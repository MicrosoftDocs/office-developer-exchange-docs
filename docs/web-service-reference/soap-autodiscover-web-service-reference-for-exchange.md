---
title: "SOAP Autodiscover web service reference for Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: "Find reference information for the SOAP Autodiscover service in Exchange."
 
 
---

# SOAP Autodiscover web service reference for Exchange

Find reference information for the SOAP Autodiscover service in Exchange.
  
The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server. You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange. Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response. 
  
> [!NOTE]
> For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service). Clients that target Exchange 2007 have to use the POX Autodiscover service. We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client. For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response. The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element. 
  
The articles in this section describe the XML instances that are sent between the client and server. The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.
  
The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples. You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running. The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.
  
This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service. 
  
## In this section
<a name="bk_InThisSection"> </a>

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## See also


- [Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Use Autodiscover to find connection points](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Get user settings from Exchange by using Autodiscover](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Get domain settings from an Exchange server](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

