---
title: "IsOrganizer"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: "The IsOrganizer element specifies a Boolean value that indicates whether this person is the organizer of the meeting."
---

# IsOrganizer

The **IsOrganizer** element specifies a Boolean value that indicates whether this person is the organizer of the meeting. 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
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
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message.  <br/> |
   
## Text value

A text value of **true** for the **IsOrganizer** element indicates that the calendar item or meeting message was created by the user. A value of **false** indicates that the calendar item or meeting message was not created bv the user. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

