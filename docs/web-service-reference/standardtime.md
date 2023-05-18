---
title: "StandardTime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: "The StandardTime element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the Bias (UTC) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed."
---

# StandardTime

The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed. 
  
- [TimeZone (Availability)](timezone-availability.md)
- [StandardTime](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 **SerializableTimeZoneTime**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Bias](bias.md) |Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time. This value is in minutes. |
|[Time](time.md) |Represents the transition time of day to and from standard time and daylight saving time. |
|[DayOrder](dayorder.md) |Represents the _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time. |
|[Month](month.md) |Represents the transition month of the year to and from standard time and daylight saving time. |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) |Represents the day of the week when the transition to and from standard time and daylight saving time occurs. |
|[Year](year.md) |Defines a time zone that changes depending on the year. This element is optional. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). |

### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) | Contains elements that identify time zone information. This element also contains information about the transition between standard time and daylight saving time. The following are the XPath expressions to this element:  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` `/GetUserAvailabilityRequest/TimeZone` |

## Remarks

The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element. When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.
  
## Example

The following example shows a region where daylight saving time is observed. The transition from daylight saving time to standard time is observed at 2 A.M. on the fifth Sunday of the tenth month.
  
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

| Element | Example |
|:-----|:-----|
|Namespace |https://schemas.microsoft.com/exchange/services/2006/types |
|Schema Name |Types schema |
|Validation File |Types.xsd |
|Can be Empty |False |

## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
