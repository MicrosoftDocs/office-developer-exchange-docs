---
title: "MeetingWorkspaceUrl"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: "The MeetingWorkspaceUrl element contains the URL for the meeting workspace that is included in the calendar item. A meeting workspace is a shared Web site for planning the meeting and tracking the results."
---

# MeetingWorkspaceUrl

The **MeetingWorkspaceUrl** element contains the URL for the meeting workspace that is included in the calendar item. A meeting workspace is a shared Web site for planning the meeting and tracking the results. 
  
```
<MeetingWorkspaceUrl/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
   
## Text value

A text value that represents a URL is required if this element is used.
  
## Remarks

The MeetingWorkspaceUrl property is read-writable for the organizer's calendar item. It is read-only for meeting requests and for attendees' calendar items.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

