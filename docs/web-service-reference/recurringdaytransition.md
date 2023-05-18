---
title: "RecurringDayTransition"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: "The RecurringDayTransition element represents a time zone transition that occurs on the same day each year."
---

# RecurringDayTransition

The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year. 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 **RecurringDayTransitionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[To](to.md) <br/> |Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.  <br/> |
|[Month (Time Zone Transition)](month-time-zone-transition.md) <br/> |Represents the month in which the time zone transition occurs.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Represents the day of the week on which the time zone transition occurs.  <br/> |
|[Occurrence (Time Zone Transition)](occurrence-time-zone-transition.md) <br/> |Represents the occurrence of the day of the week in the month that the time zone transition occurs.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |Represents a collection of time zone transitions.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Represents a collection of time zone transitions.  <br/> |
   
## Remarks

An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

