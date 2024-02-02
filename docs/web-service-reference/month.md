---
title: "Month"
description: "The Month element represents the transition month of the year to and from standard time and daylight saving time."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
---

# Month

The **Month** element represents the transition month of the year to and from standard time and daylight saving time. 
  
```xml
<Month>...</Month>
```

**Short**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed. <br/> <br/>  The following are the XPath expressions to the [StandardTime](standardtime.md) element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  <br/><br/>  The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## Text value

A text value is required. The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12. A value of 0 is used in the Timezone–StandardTime–Month and Timezone–DaylightTime–Month elements if the timezone does not observe DST. This is a short integer data type.
  
## Remarks

A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month. 
  
## Element information

|Item|Value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [Getting User Availability](/previous-versions/office/developer/exchange-server-2010/aa494212(v=exchg.140))
