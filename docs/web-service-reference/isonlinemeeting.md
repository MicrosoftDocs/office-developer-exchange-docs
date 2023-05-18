---
title: "IsOnlineMeeting"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsOnlineMeeting
api_type:
- schema
ms.assetid: c29df676-0f3a-4694-a42f-522c6d16872f
description: "The IsOnlineMeeting element indicates whether the meeting is online."
---

# IsOnlineMeeting

The **IsOnlineMeeting** element indicates whether the meeting is online. 
  
```xml
<IsOnlineMeeting/>
```

 **Boolean**
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

A text value that represents a Boolean value is required if this element is used. A value of **true** indicates that the meeting is online. A value of **false** indicates that the meeting is not online. 
  
## Remarks

The IsOnlineMeeting property is read-only.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

