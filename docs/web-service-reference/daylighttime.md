---
title: "DaylightTime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: "The DaylightTime element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the Bias (UTC) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs."
---

# DaylightTime

The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs. 
  
- [TimeZone (Availability)](timezone-availability.md) 
- [DaylightTime](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
```

**SerializableTimeZoneTime**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Bias](bias.md) <br/> |Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time. This value is in minutes.  <br/> |
|[Time](time.md) <br/> |Represents the transition time of day to and from standard time and daylight saving time.  <br/> |
|[DayOrder](dayorder.md) <br/> |Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.  <br/> |
|[Month](month.md) <br/> |Represents the transition month of the year to and from standard time and daylight saving time.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Represents the day of the week when the transition to and from standard time and daylight saving time occurs.  <br/> |
|[Year](year.md) <br/> |Used to define a time zone that changes depending on the year. This element is optional. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | Contains elements that identify time zone information.<br/><br/>This element also contains information about the transition between standard time and daylight saving time.<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## Example

The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## Element information

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

