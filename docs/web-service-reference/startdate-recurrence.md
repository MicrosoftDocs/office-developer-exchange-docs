---
title: "StartDate (Recurrence)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: "The StartDate element represents the start date of a recurring task or calendar item."
---

# StartDate (Recurrence)

The **StartDate** element represents the start date of a recurring task or calendar item. 
  
```xml
<StartDate/>
```

**Date**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describes the start date and the end date of an item recurrence pattern.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describes the start date of an item recurrence pattern that does not have a defined end date.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describes the start date and the number of occurrences of a recurring item.  <br/> |
   
## Text value

A text value that represents a date is required if this element is used. The value cannot be less than Apr, 1, 1601 00:00:00.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

