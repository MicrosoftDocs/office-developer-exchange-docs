---
title: "DaysOfWeek (DaysOfWeekType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: "The DaysOfWeek (DaysOfWeekType) element describes days of the week that are used in item recurrence patterns."
---

# DaysOfWeek (DaysOfWeekType)

The **DaysOfWeek** element describes days of the week that are used in item recurrence patterns. 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describes a weekly recurrence pattern.  <br/> |
   
## Text value

A text value is required. The following are the possible values:
  
- Sunday    
- Monday    
- Tuesday    
- Wednesday    
- Thursday    
- Friday    
- Saturday    
- Day (this value is not valid for a weekly recurrence pattern)    
- Weekday (this value is not valid for a weekly recurrence pattern)    
- WeekendDay (this value is not valid for a weekly recurrence pattern)
    
A weekly recurrence pattern can contain multiple values. Values are separated by a space character. For example, for a weekly recurrence on Tuesdays and Thursdays, the text value will be "Tuesday Thursday".
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

