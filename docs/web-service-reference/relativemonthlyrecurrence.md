---
title: "RelativeMonthlyRecurrence"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RelativeMonthlyRecurrence
api_type:
- schema
ms.assetid: a76595db-7460-44ac-ac2a-53241caa33a7
description: "The RelativeMonthlyRecurrence element describes a relative monthly recurrence pattern."
---

# RelativeMonthlyRecurrence

The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern. 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 **RelativeMonthlyRecurrencePatternType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Interval](interval.md) <br/> |Defines the interval between two consecutive monthly recurring pattern items. The range for this value is 1 to 99.  <br/> |
|[DaysOfWeek (DayOfWeekType)](daysofweek-dayofweektype.md) <br/> |Describes which days of the week are in the relative monthly recurrence pattern.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Describes which week is used in a relative monthly recurrence pattern.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contains the recurrence pattern for calendar items and meeting requests.  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contains recurrence information for recurring tasks.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

