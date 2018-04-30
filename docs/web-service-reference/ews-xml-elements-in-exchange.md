---
title: "EWS XML elements in Exchange"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: "Find reference information for the EWS XML elements in Exchange."
---

# EWS XML elements in Exchange

Find reference information for the EWS XML elements in Exchange.
  
Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements. The documentation in this section is based on the XML instances that are sent between the client and server. The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS. If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:
  
- http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.
    
- http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.
    
- http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.
    
The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions. The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.
  
The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition. This is because EWS is not designed to be hosted on a computer that has a predefined address. You can use the Autodiscover service to get the EWS endpoint address. Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition. If your object model generator encounters an error, you can insert a placeholder WSDL service definition.
  
> [!TIP]
> If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator. The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML. For more information, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body. With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation. The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.
  
## Additional resources
<a name="bk_addresources"> </a>

- [EWS reference for Exchange](ews-reference-for-exchange.md)
    
- [EWS operations in Exchange](ews-operations-in-exchange.md)
    
- [Explore the EWS Managed API, EWS, and web services in Exchange](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx)
    
- [Start using web services in Exchange](http://msdn.microsoft.com/library/e1b07a92-0595-4bf1-bd6b-c07e66a8c923%28Office.15%29.aspx)
    
- [Autodiscover for Exchange](http://msdn.microsoft.com/library/da0f9402-4e35-42c7-a15e-1e9e4e966e8b%28Office.15%29.aspx)
    

