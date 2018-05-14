---
title: "SOAP Autodiscover XML elements for Exchange 2013"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: "Find XML element reference information for the SOAP Autodiscover web service in Exchange."
 
 
---

# SOAP Autodiscover XML elements for Exchange 2013

Find XML element reference information for the SOAP Autodiscover web service in Exchange.
  
The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server. This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service. Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:
  
- http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl — The location of the WSDL file.
    
- http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd — The location of the messages schema.
    
The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.
  
The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body. This file provides a general roadmap of what the XML structure can be for a given request-response message interaction. The actual XML structure that is sent between the client and server is based on the options and the context in which it is used. The schema files define what XML is possible. The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings. 
  
## Related sections
<a name="bk_RelatedSections"> </a>

- [SOAP Autodiscover web service reference for Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [EWS reference for Exchange](ews-reference-for-exchange.md)
    
- [Unified Messaging web service reference for Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## See also

- [Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

