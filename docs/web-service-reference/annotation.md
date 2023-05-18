---
title: "Annotation"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e0392635-9d0f-46d5-84ef-0a8a3036479a
description: "The Annotation element contains optional notes added by a user."
---

# Annotation

The **Annotation** element contains optional notes added by a user. 
  
```XML
<Annotation></Annotation>
```

 **xs:string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EnhancedLocation](enhancedlocation.md) <br/> |Specifies location information such as the name, address, and optional notes about a location.  <br/> |
   
## Text value

The text value of the Annotation element is a user added note about a location.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

