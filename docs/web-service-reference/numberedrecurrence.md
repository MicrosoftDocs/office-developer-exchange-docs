---
title: "NumberedRecurrence"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- NumberedRecurrence
api_type:
- schema
ms.assetid: 53746909-ef21-4764-8715-a7769b943cca
description: "The NumberedRecurrence element describes the start date and the number of occurrences of a recurring item."
---

# NumberedRecurrence

The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item. 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 **NumberedRecurrenceRangeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[StartDate (Recurrence)](startdate-recurrence.md) <br/> |Represents the start date of a recurring task or calendar item.  <br/> |
|[NumberOfOccurrences](numberofoccurrences.md) <br/> |Contains the number of occurrences of a recurring item.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contains the recurrence pattern for calendar items and meeting requests.  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contains recurrence information for recurring tasks.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

