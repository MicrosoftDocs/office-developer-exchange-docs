---
title: "End" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: "The End element represents the end of a duration."
---

# End

The **End** element represents the end of a duration. 
  
```xml
<End/>
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
|[CalendarItem](calendaritem.md)|Represents an Exchange calendar item. |
|[FirstOccurrence](firstoccurrence.md)|Represents the first occurrence of a recurring calendar item. |
|[LastOccurrence](lastoccurrence.md)|Represents the last occurrence of a recurring calendar item. |
|[MeetingRequest](meetingrequest.md)|Represents a meeting request in the Exchange store. |
|[Occurrence](occurrence.md)|Represents a single modified occurrence of a recurring calendar item. |

## Text value

The text value represents the end of a duration.
  
## Remarks

The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item. In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time. This can cause an error if the [Start](start.md) time is later than the **End** time. Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.
  
> [!NOTE]
> The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace |https://schemas.microsoft.com/exchange/services/2006/types |
|Schema Name |Types schema |
|Validation File |Types.xsd |
|Can be Empty |False |

## See also

[WeeklyRecurrence](weeklyrecurrence.md)
  
**End**

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
