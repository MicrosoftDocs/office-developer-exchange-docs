---
title: "Recurrence (RecurrenceType)"
 
 
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
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: "The Recurrence element contains the recurrence pattern for calendar items and meeting requests."
---

# Recurrence (RecurrenceType)

The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests. 
  
```
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 **RecurrenceType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describes a relative yearly recurrence pattern.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Represents a yearly recurrence pattern.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describes a relative monthly recurrence pattern for a recurring calendar item.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Represents a monthly recurrence pattern.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describes the frequency, in weeks, and the days that a calendar item or task recurs.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describes the frequency, in days, in which a calendar item or task recurs.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describes a recurrence pattern that does not have a defined end date.  <br/> The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describes the start date and the end date of an item recurrence pattern.  <br/> The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describes the start date and the number of occurrences of a recurring item.  <br/> The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store  <br/> |
   
## Remarks

This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value. 
  
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

