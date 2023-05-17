---
title: "DisplayNameLastFirstHeader"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ca77431e-2d6c-48e0-a20e-e8616c6fa157
description: "The DisplayNameLastFirstHeader element specifies the header for the display name, last name first."
---

# DisplayNameLastFirstHeader

The **DisplayNameLastFirstHeader** element specifies the header for the display name, last name first. 
  
```xml
<DisplayNameLastFirstHeader></DisplayNameLastFirstHeader>
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

The text value of the **DisplayNameLastFirstHeader** element is a string value that specifies the display name, surname first. 
  
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

