---
title: "Month (Time Zone Transition)"
 
 
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
ms.assetid: 5e6aac75-366d-43d0-8ccb-956285474662
description: "The Month element represents the month in which the time zone transition occurs."
---

# Month (Time Zone Transition)

The **Month** element represents the month in which the time zone transition occurs. 
  
```xml
<Month/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Represents a time zone transition that occurs on a specific date each year.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Represents a time zone transition that occurs on the same day each year.  <br/> |
   
## Text value

The text value is an integer that represents the month in which the time zone transition occurs.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

