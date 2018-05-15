---
title: "Recurrence (TaskRecurrenceType)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: "The Recurrence element contains recurrence information for recurring tasks."
---

# Recurrence (TaskRecurrenceType)

The **Recurrence** element contains recurrence information for recurring tasks. 
  
```
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 **TaskRecurrenceType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describes a relative yearly recurrence pattern for a recurring task.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Represents a yearly recurrence pattern for a recurring task.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describes a relative monthly recurrence pattern for a recurring task.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Represents a monthly recurrence pattern for a recurring task.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describes the frequency, in weeks, and the days on which a task recurs.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describes the frequency, in days, in which a task recurs.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describes how many days after the completion of the current task the next occurrence will be due.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describes how many weeks after the completion of the current task the next occurrence will be due.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describes how many months after the completion of the current task the next occurrence will be due.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describes how many years after the completion of the current task the next occurrence will be due.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describes a recurrence pattern that does not have a defined end date.  <br/> The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describes the start date and the end date of an item recurrence pattern.  <br/> The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.  <br/> [EndDateRecurrence](enddaterecurrence.md) cannot be used together with a regeneration pattern.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describes the start date and the number of occurrences of a recurring item.  <br/> The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
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



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

