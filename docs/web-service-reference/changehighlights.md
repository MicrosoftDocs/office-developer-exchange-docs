---
title: "ChangeHighlights"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: "The ChangeHighlights element specifies what has changed between two versions of a meeting request message."
---

# ChangeHighlights

The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message. 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 **ChangeHighlightsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[HasLocationChanged](haslocationchanged.md) <br/> |Specifies whether the location property of a meeting has changed.  <br/> |
|[Location](location.md) <br/> |Represents the location of a meeting or appointment.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Specifies whether the start time for a meeting has changed.  <br/> |
|[Start](start.md) <br/> |Represents the start of a duration.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Specifies whether the end time for a meeting has changed.  <br/> |
|[End ](end-ex15websvcsotherref.md) <br/> |Represents the end of a duration.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
   
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

