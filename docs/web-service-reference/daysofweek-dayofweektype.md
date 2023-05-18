---
title: "DaysOfWeek (DayOfWeekType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: ba8f990d-d37d-403d-b31f-55e5208c8ad5
description: "The DaysOfWeek (DayOfWeekType) element describes days of the week that are used in item recurrence patterns."
---

# DaysOfWeek (DayOfWeekType)

The **DaysOfWeek** element describes days of the week that are used in item recurrence patterns. 
  
```xml
<DaysOfWeek/>
```

**DayOfWeekType**

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
  
- Sunday    
- Monday    
- Tuesday   
- Wednesday    
- Thursday    
- Friday    
- Saturday    
- Day (not used in the TimeChangePatternTypes)    
- Weekday (not used in the TimeChangePatternTypes)    
- WeekendDay (not used in the TimeChangePatternTypes)
    
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

