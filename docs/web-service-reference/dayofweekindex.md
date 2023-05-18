---
title: "DayOfWeekIndex"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DayOfWeekIndex
api_type:
- schema
ms.assetid: 82420338-a1f7-4887-b338-b2d93b2c2bf1
description: "The DayOfWeekIndex element describes which week in a month is used in a relative recurrence pattern."
---

# DayOfWeekIndex

The **DayOfWeekIndex** element describes which week in a month is used in a relative recurrence pattern. 
  
```xml
<DayOfWeekIndex/>
```

**DayOfWeekIndexType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describes a relative yearly recurrence pattern.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describes a relative monthly recurrence pattern.  <br/> |
   
## Text value

A text value is required. The following are the possible values:
  
- First    
- Second    
- Third    
- Fourth    
- Last
    
## Remarks

For example, the second Monday of a month may occur in the third week of that month. If a month starts on a Friday, the first week of the month only contains a few days and does not contain a Monday. Therefore, the first Monday would have to occur in the second week.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

