---
title: "IsHidden"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: "The IsHidden element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona."
---

# IsHidden

The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona. 
  
```XML
<IsHidden>true | false</IsHidden>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Specifies an instance in an array of attributes for a **Persona** element.  <br/> |
   
## Text value

A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona. A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona. 
  
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

