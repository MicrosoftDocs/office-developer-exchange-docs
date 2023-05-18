---
title: "AllowNewTimeProposal"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: "The AllowNewTimeProposal element indicates whether a new meeting time can be proposed for a meeting by an attendee."
---

# AllowNewTimeProposal

The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee. 
  
```xml
<AllowNewTimeProposal/>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
   
## Text value

A text value that represents a Boolean value is required. A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed. The organizer sets this value in the meeting request. 
  
## Remarks

The AllowNewTimeProposal property is read-writable for the organizer's calendar item. It is read-only for meeting requests and for attendees' calendar items.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
> [!NOTE]
> Exchange Web Services does not support new time proposal messages. To get properties that are related to new time proposal messages, use extended properties. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

