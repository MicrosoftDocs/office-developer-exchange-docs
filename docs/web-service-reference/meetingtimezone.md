---
title: "MeetingTimeZone"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MeetingTimeZone
api_type:
- schema
ms.assetid: 413b47d9-8126-462c-9a4f-4e771a5e8889
description: "The MeetingTimeZone element represents the time zone of the location where the meeting is hosted."
---

# MeetingTimeZone

The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted. 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 **TimeZoneType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**TimeZoneName** <br/> |Describes the name of the time zone.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[BaseOffset](baseoffset.md) <br/> |Represents the hourly offset from UTC for the current time zone.  <br/> |
|[Standard](standard.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
|[Daylight](daylight.md) <br/> |Represents the date and time when the time changes from standard time to daylight saving time.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

