---
title: "IsQuickContact"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: "The IsQuickContact element specifies a Boolean value that indicates whether the underlying contact is a quick contact."
---

# IsQuickContact

The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact. 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 **boolean**
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

A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact. A value of **false** indicates that the contact is not a quick contact. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> |false  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

