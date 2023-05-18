---
title: "MaximumBodySize"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: cc52f7f5-c2a8-4cfb-937b-dfec6cd3ea0f
description: "The MaximumBodySize element specifies the maximum size of the item body to return in a response."
---

# MaximumBodySize

The **MaximumBodySize** element specifies the maximum size of the item body to return in a response. 
  
```XML
<MaximumBodySize></MaximumBodySize>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ItemShape](itemshape.md)
  
## Text value

The text value of the **MaximumBodySize** element indicates the maximum size of the [Body](body.md) property returned in the response. This is measured in kilobytes. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

