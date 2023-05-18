---
title: "StartTimeZone"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: "The StartTimeZone element defines the time zone for the start time of a CalendarItem or MeetingRequest."
---

# StartTimeZone

The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

**TimeZoneDefinitionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Represents the unique identifier of the time zone definition.  <br/> |
|Name  <br/> |Represents the descriptive name of the time zone definition.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Periods](periods.md) <br/> |Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.  <br/> |
|[Transitions](transitions.md) <br/> |Represents an array of time zone transitions.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

