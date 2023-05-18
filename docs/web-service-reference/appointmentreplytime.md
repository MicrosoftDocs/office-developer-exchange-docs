---
title: "AppointmentReplyTime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AppointmentReplyTime
api_type:
- schema
ms.assetid: 7784468c-c863-488a-864b-ce4d6c671dbe
description: "The AppointmentReplyTime element represents the date and time that an attendee replied to a meeting request."
---

# AppointmentReplyTime

The **AppointmentReplyTime** element represents the date and time that an attendee replied to a meeting request. 
  
```xml
<AppointmentReplyTime/>
```

 **DateTime**
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
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
   
## Text value

A string that represents a date and time.
  
## Remarks

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

