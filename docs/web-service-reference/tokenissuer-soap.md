---
title: "TokenIssuer (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: "The TokenIssuer element specifies the Uri (SOAP) and Endpoint (SOAP) for the security token service."
 
 
---

# TokenIssuer (SOAP)

The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service. 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Uri (SOAP)](uri-soap.md) <br/> |The URI of the security token service that issued the security token.  <br/> |
|[Endpoint (SOAP)](endpoint-soap.md) <br/> |The web service Endpoint URI.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).  <br/> |
   
## Remarks

Use the **TokenIssuer** element to specify the security token service when using security tokens. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

