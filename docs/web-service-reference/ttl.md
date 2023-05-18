---
title: "TTL"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: cfefc053-1e3c-46fb-8014-b56a654f2fb3
description: "The TTL element specifies the time, in minutes, that the token is valid."
---

# TTL

The **TTL** element specifies the time, in minutes, that the token is valid. 
  
```XML
<TTL></TTL>
```

 **integer**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Token](token.md)
  
## Text value

The text value of the **TTL** element is the time in minutes that the token is valid. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
