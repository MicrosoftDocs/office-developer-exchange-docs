---
title: "Endpoint (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 630cdbb5-d1c7-422c-924a-abf5738e9e5e
description: "The Endpoint element specifies the security token service endpoint."
 
 
---

# Endpoint (SOAP)

The **Endpoint** element specifies the security token service endpoint. 
  
```XML
<Endpoint/>
```

 **xs:anyURI**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

None
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Specifies the URI and Endpoint for the security token service.  <br/> |
   
## Text value

The text value represents the endpoint for the security token web service.
  
## Remarks

The endpoint is used for communicating with the security token web service.
  
## Element information

|Name|Value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Auto-discover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   

