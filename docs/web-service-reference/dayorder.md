---
title: "DayOrder"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: "The DayOrder element represents the nth occurrence of the day specified in the DayOfWeek (TimeZone) element that represents the date of transition from and to standard time and daylight saving time."
---

# DayOrder

The **DayOrder** element represents the _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.
  
```xml
<DayOrder>...</DayOrder>
```

**short**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[StandardTime](standardtime.md) | Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.<br/>This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.<br/>The following are the XPath expressions to the [StandardTime](standardtime.md) element:<br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` |
|[DaylightTime](daylighttime.md) | Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.<br/>This element also contains information about when the transition to daylight saving time from standard time occurs.<br/>The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:<br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` |

## Text value

A text value is required. The value for the **DayOrder** element can be 1 through 5. The maximum value for this element can be either 4 or 5, depending on the month and year. A value of 0 is used in the Timezone–StandardTime–DayOrder and Timezone–DaylightTime–DayOrder elements if the timezone does not observe DST.
  
## Remarks

A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  |https://schemas.microsoft.com/exchange/services/2006/types  |
|Schema Name  |Types schema  |
|Validation File  |Types.xsd  |
|Can be Empty  |False  |

## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
