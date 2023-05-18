---
title: "Start"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: "The Start element represents the start of a duration."
---

# Start

The **Start** element represents the start of a duration. 
  
```xml
<Start/>
```

**DateTime**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[DeletedOccurrence](deletedoccurrence.md) <br/> |Represents a deleted occurrence of a recurring calendar item.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Represents the first occurrence of a recurring calendar item.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Represents the last occurrence of a recurring calendar item.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[Occurrence](occurrence.md) <br/> |Represents a single modified occurrence of a recurring calendar item.  <br/> |
   
## Text value

The text value represents the start of a duration.
  
## Remarks

The UpdateItem operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item. In an UpdateItem request, the **Start** time can be set without also setting the **End** time. This can cause an error if the **Start** time is later than the **End** time. Be aware that client applications must perform adjustments to **End** time when that **Start** time is changed in order to preserve the duration. 
  
> [!NOTE]
> The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Code**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [WeeklyRecurrence](weeklyrecurrence.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

