---
title: "Bias (UTC)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: "The Bias element represents the general offset from Coordinated Universal Time (UTC). This value is in minutes."
---

# Bias (UTC)

The **Bias** element represents the general offset from Coordinated Universal Time (UTC). This value is in minutes. 
  
```
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | The container that identifies the date-time information of the request. This element contains information about the transition between standard time and daylight saving time.  <br/>  The following are the XPath expressions to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/>  `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## Text value

A text value is required. The text value represents an integer.
  
## Remarks

A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset. 
  
## Example

The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.
  
```
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetUserAvailability operation](getuseravailability-operation.md)
  
[Bias](bias.md)
#### Other resources

[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

