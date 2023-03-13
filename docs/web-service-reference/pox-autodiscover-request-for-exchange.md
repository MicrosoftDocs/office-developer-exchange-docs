---
title: "POX Autodiscover request for Exchange"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: "The Autodiscover request contains a query for a user's client access configuration."
 
 
---

# POX Autodiscover request for Exchange

The Autodiscover request contains a query for a user's client access configuration.
  
## Autodiscover request example

### Description

The following XML example shows an Autodiscover request body.
  
### Code

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### Request Headers

The following HTTP headers are optional when sending Autodiscover requests.
  
**Table 1. HTTP request headers**

|**Header**|**Description**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol. This header is applicable to clients that implement the MAPI/HTTP protocol.  <br/> |
|X-ClientCanHandle  <br/> |This header contains a comma-delimited list of capabilities that the client supports. The possible values are specified in Table 2.  <br/> |
   
**Table 2. X-ClientCanHandle header values**

|**X-ClientCanHandle value (case-insensitive)**|**Minimum server version**|**Description**|
|:-----|:-----|:-----|
|Negotiate  <br/> |15.00.0995.014  <br/> |If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication. If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections. If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".  <br/> |
   
### Request elements

The following elements are used in the request body:
  
- [AutoDiscover (POX)](autodiscover-pox.md)
    
- [Request (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element. 
  
### Version differences

The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).
  
The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.
  
## See also



[POX Autodiscover response for Exchange](pox-autodiscover-response-for-exchange.md)


[POX Autodiscover web service reference for Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

