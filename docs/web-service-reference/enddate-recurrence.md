---
title: "EndDate (Recurrence)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- EndDate
api_type:
- schema
ms.assetid: 16026595-26f8-4770-8a6d-0d3e4157effd
description: "The EndDate element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type."
---

# EndDate (Recurrence)

The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type. 
  
```
<EndDate/>
```

 **date**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describes the start date and the end date of an item recurrence pattern.  <br/> |
   
## Text value

A text value that represents a date is required if this element is used. The value cannot be larger than September 1, 4500 00:00:00.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

