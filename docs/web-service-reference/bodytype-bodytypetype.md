---
title: "BodyType (BodyTypeType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d730e3af-3102-4242-a2f1-c2873af188f9
description: "The BodyType element specifies the type of the body of the item."
---

# BodyType (BodyTypeType)

The **BodyType** element specifies the type of the body of the item. 
  
```XML
<BodyType> HTML | Text</BodyType>
```

 **BodyTypeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Body](body.md) <br/> |Specifies the body of an item.  <br/> |
   
## Text value

**BodyType element text values**

|**Value**|**Description**|
|:-----|:-----|
|HTML  <br/> |Indicates that the body is HTML.  <br/> |
|Text  <br/> |Indicates that the body is text.  <br/> |
   
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

