---
title: "EndDateRecurrence"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: "The EndDateRecurrence element describes the start date and the end date of an item recurrence pattern."
---

# EndDateRecurrence

The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern. 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 **EndDateRecurrenceRangeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[StartDate (Recurrence)](startdate-recurrence.md) <br/> |Represents the start date of a recurring task or calendar item.  <br/> |
|[EndDate (Recurrence)](enddate-recurrence.md) <br/> |Represents the end date of a recurring task or calendar item.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contains the recurrence pattern for calendar items and meeting requests.  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contains the recurrence pattern for recurring tasks.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

