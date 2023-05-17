---
title: "Interval"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: "The Interval element defines the interval between two consecutive recurring items."
---

# Interval

The **Interval** element defines the interval between two consecutive recurring items. 
  
```xml
<Interval/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Represents a monthly recurrence pattern.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describes the frequency, in days, in which a task is regenerated.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describes the frequency, in days, in which a task recurs.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describes the frequency, in months, in which a task is regenerated.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describes a relative monthly pattern for a recurring task.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describes the frequency, in weeks, in which and the days on which a task recurs.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describes the frequency, in weeks, in which a task is regenerated.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describes the frequency, in years, in which a task is regenerated.  <br/> |
   
## Text value

A text value that represents an integer is required.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

