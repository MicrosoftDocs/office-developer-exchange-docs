---
title: "RequestType"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: "The RequestType element identifies whether a proxy request is a cross-site or a cross-forest request."
---

# RequestType

The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request. 
  
```
<RequestType>CrossSite or CrossForest</RequestType>
```

 **AvailabilityProxyRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

This element does not have a parent in the schema. This element is used in the SOAP header. For more information about how this element is used, see the WSDL file.
  
## Text value

A text value is required for this element. The following are the possible values:
  
- CrossSite
    
- CrossForest
    
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

