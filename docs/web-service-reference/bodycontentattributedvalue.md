---
title: "BodyContentAttributedValue"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f99e9590-8388-4203-ac30-1ea394f351a6
description: "The BodyContentAttributedValue element specifies the body content of an item."
---

# BodyContentAttributedValue

The **BodyContentAttributedValue** element specifies the body content of an item. 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 **BodyContentAttributedValueType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Value (BodyContentType)](value-bodycontenttype.md) <br/> |Specifies the value of a **BodyContentAttributedValue** element.  <br/> |
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Specifies an array of attribution information for one or more of the contacts or active directory recipients aggregated into the associated persona.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Bodies](bodies.md) <br/> |Specifies an array of **BodyContentAttributedValue** elements.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

