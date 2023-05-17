---
title: "RecurringDateTransition"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: "The RecurringDateTransition element represents a time zone transition that occurs on a specific date each year."
---

# RecurringDateTransition

The **RecurringDateTransition** element represents a time zone transition that occurs on a specific date each year. 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 **RecurringDateTransitionType**
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
|[Day](day.md) <br/> |Represents the day of the month on which the time zone transition occurs.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |Represents a collection of time zone transitions.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Represents a collection of time zone transitions.  <br/> |
   
## Remarks

An example of a time zone transition that could be represented by the [RecurringDateTransition](recurringdatetransition.md) element is a transition that occurs on March 15 each year. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

