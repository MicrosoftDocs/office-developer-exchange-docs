---
title: "Occurrence (Time Zone Transition)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: "The Occurrence element represents the occurrence of the day of the week in the month that the time zone transition occurs."
---

# Occurrence (Time Zone Transition)

The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs. 
  
```xml
<Occurrence/>
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
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Represents a time zone transition that occurs on the same day each year.  <br/> |
   
## Text value

The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs. The following table lists the possible values.
  
|**Value**|**Description**|
|:-----|:-----|
|1  <br/> |The first occurrence of the specified day of the week from the beginning of the month.  <br/> |
|2  <br/> |The second occurrence of the specified day of the week from the beginning of the month.  <br/> |
|3  <br/> |The third occurrence of the specified day of the week from the beginning of the month.  <br/> |
|4  <br/> |The fourth occurrence of the specified day of the week from the beginning of the month.  <br/> |
|-1  <br/> |The first occurrence of the specified day of the week from the end of the month.  <br/> |
|-2  <br/> |The second occurrence of the specified day of the week from the end of the month.  <br/> |
|-3  <br/> |The third occurrence of the specified day of the week from the end of the month.  <br/> |
|-4  <br/> |The fourth occurrence of the specified day of the week from the end of the month.  <br/> |
   
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

