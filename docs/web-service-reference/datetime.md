---
title: "DateTime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DateTime
api_type:
- schema
ms.assetid: 9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4
description: "The DateTime element represents the date and time at which the time zone transition occurs."
---

# DateTime

The **DateTime** element represents the date and time at which the time zone transition occurs. 
  
```xml
<DateTime/>
```

**DateTime**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Represents a time zone transition that occurs on a specific date and at a specific time.  <br/> |
   
## Text value

The text value of the **DateTime** element represents the date and time at which the time zone transition occurs. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

