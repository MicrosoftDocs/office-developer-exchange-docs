---
title: "ConflictingMeetingCount"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: "The ConflictingMeetingCount element represents the number of meetings that conflict with the calendar item."
---

# ConflictingMeetingCount

The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item. 
  
```xml
<ConflictingMeetingCount/>
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
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
   
## Text value

The text value represents an integer. This property is read-only.
  
## Remarks

A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder. If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder. Meeting requests are compared with calendar items in the default calendar folder.
  
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

