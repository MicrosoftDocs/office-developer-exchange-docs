---
title: "BaseShape (PreviewItemBaseShapeType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7b9e2fdd-5678-4178-9297-7f12a3ca9d64
description: "The BaseShape element specifies either the default preview with all properties returned or a compact preview with fewer properties returned."
---

# BaseShape (PreviewItemBaseShapeType)

The **BaseShape** element specifies either the default preview with all properties returned or a compact preview with fewer properties returned. 
  
```XML
<BaseShape> Default | Compact</BaseShape>
```

 **PreviewItemBaseShapeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PreviewItemResponseShape](previewitemresponseshape.md) <br/> |Contains the shape of the response.  <br/> |
   
## Text value

**BaseShape element text values**

|**Value**|**Description**|
|:-----|:-----|
|Default  <br/> |Indicates that all properties are shown.  <br/> |
|Compact  <br/> |Indicates that only selected properties are shown.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

