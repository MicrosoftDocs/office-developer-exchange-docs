---
title: "POX Autodiscover web service reference for Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: "Find reference information for the POX Autodiscover service in Exchange."
 
 
---

# POX Autodiscover web service reference for Exchange

Find reference information for the POX Autodiscover service in Exchange.
  
The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server. You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.
  
> [!NOTE]
> For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service. Clients that target Exchange 2007 have to use the POX Autodiscover service. We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client. For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response. The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element. This documentation covers the XML instances that are sent between the client and server. The POX Autodiscover service does not have an explicit schema.
  
The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service. 
  
## In this section
<a name="bk_InThisSection"> </a>

- [POX Autodiscover request for Exchange](pox-autodiscover-request-for-exchange.md)
    
- [POX Autodiscover response for Exchange](pox-autodiscover-response-for-exchange.md)
    
- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## See also

- [Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [SOAP Autodiscover web service reference for Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

