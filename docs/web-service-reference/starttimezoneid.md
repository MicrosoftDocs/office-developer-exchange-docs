---
title: "StartTimeZoneId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f4adfc48-2d51-4d2d-9ddc-b91c3e96cb02
description: "The StartTimeZoneId element specifies the time zone in which a meeting takes place."
---

# StartTimeZoneId

The **StartTimeZoneId** element specifies the time zone in which a meeting takes place. 
  
```XML
<StartTimeZoneId></StartTimeZoneId>
```

**string**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[CalendarItem](calendaritem.md) | [MeetingRequest](meetingrequest.md)
  
## Text value

The text value of the **StartTimeZoneId** element is the time zone identifier of the time zone used in the [Start](start.md) element. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

