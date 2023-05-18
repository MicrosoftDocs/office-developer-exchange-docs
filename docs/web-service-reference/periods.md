---
title: "Periods"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: "The Periods element represents an array of periods that define the time offset at different stages of the time zone."
---

# Periods

The **Periods** element represents an array of periods that define the time offset at different stages of the time zone. 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 **NonEmptyArrayOfPeriodsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Period](period.md) <br/> |Defines the name, time offset, and unique identifier for a specific stage of the time zone.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Defines a time zone.  <br/> |
   
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

