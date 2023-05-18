---
title: "DisplayNamePrefix"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 60363698-7603-4051-a66e-007c02db17cb
description: "The DisplayNamePrefix element specifies the prefix of the display name of the associated persona."
---

# DisplayNamePrefix

The **DisplayNamePrefix** element specifies the prefix of the display name of the associated persona. 
  
```xml
<DisplayNamePrefix></DisplayNamePrefix>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Specifies a set of persona data returned by a **GetPersona** request.  <br/> |
   
## Text value

The text value of the **DisplayNamePrefix** element is a string value that specifies the prefix for the display name. 
  
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

