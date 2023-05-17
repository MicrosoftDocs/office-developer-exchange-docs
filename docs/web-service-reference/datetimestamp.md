---
title: "DateTimeStamp"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DateTimeStamp
api_type:
- schema
ms.assetid: c996c319-28f1-4bed-ab7a-4d0fc866e675
description: "The DateTimeStamp element indicates the date and time that an instance of a calendar object was created."
---

# DateTimeStamp

The **DateTimeStamp** element indicates the date and time that an instance of a calendar object was created. 
  
```xml
<DateTimeStamp/>
```

**dateTime**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation.  <br/> |
   
## Text value

The text value represents a date/time value that identifies a calendar occurrence.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

