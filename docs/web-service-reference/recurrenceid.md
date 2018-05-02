---
title: "RecurrenceId"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: "The RecurrenceId element is used to identify a specific instance of a recurring calendar item."
---

# RecurrenceId

The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item. 
  
```
<RecurrenceId/>
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation.  <br/> |
   
## Text value

The text value represents a date/time value that identifies a calendar occurrence.
  
## Remarks

This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

