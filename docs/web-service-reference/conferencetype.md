---
title: "ConferenceType"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConferenceType
api_type:
- schema
ms.assetid: 6bcf6c18-2695-44b1-aabe-dadc52b2633a
description: "The ConferenceType element describes the type of conferencing that is performed with a calendar item."
---

# ConferenceType

The **ConferenceType** element describes the type of conferencing that is performed with a calendar item. 
  
```xml
<ConferenceType/>
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
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
   
## Text value

A text value that represents an integer value is required if this element is used. The following are the possible values for this element:
  
- 0 = NetMeeting
    
- 1 = NetShow
    
- 2 = Chat
    
## Remarks

The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item. It is read-only for meeting requests and for attendee's calendar items. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

