---
title: "Daylight"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: "The Daylight element represents the date and time when the time changes from standard time to daylight saving time."
---

# Daylight

The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time. 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

**TimeChangeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**TimeZoneName** <br/> |Describes the name of the time zone.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Describes the offset from the [BaseOffset](baseoffset.md). The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describes a relative yearly recurrence pattern for a time zone transition date pattern.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Represents the date when the time changes from standard or daylight saving time.  <br/> |
|[Time (TimeChangeType)](time-timechangetype.md) <br/> |Describes the time when the time changes between standard time and daylight saving time.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Represents the time zone of the location where the meeting is hosted.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

