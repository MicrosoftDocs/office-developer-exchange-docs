---
title: "AppointmentState"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: "The AppointmentState element specifies the status of the appointment."
---

# AppointmentState

The **AppointmentState** element specifies the status of the appointment. 
  
```XML
<AppointmentState/>
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
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
   
## Text value

This element contains a text value that represents set bits. This is in integer form. This element is read-only. It will only be returned in a response.
  
## Remarks

The integer value that is returned represents the appointment state bitmask. The following table describes each bit.
  
|**Name**|**Bit**|**Description**|
|:-----|:-----|:-----|
|None  <br/> |0x0000  <br/> |No flags have been set. This is only used for an appointment that does not include attendees.  <br/> |
|Meeting  <br/> |0x0001  <br/> |This appointment is a meeting.  <br/> |
|Received  <br/> |0x0002  <br/> |This appointment has been received.  <br/> |
|Canceled  <br/> |0x0004  <br/> |This appointment has been canceled.  <br/> |
   
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

