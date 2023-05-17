---
title: "IsRecurring"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: "The IsRecurring element indicates whether a calendar item, meeting request, or task is part of a recurring item. This element is read-only."
---

# IsRecurring

The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item. This element is read-only. 
  
```xml
<IsRecurring/>
```

 **Boolean**
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
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

A text value that represents a Boolean value is required.
  
## Remarks

The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates. 
  
|**CalendarItem Type**|**Organizer  <br/> (IsRecurring)**|**Attendee  <br/> (IsRecurring)**|**Meeting request/update  <br/> (IsRecurring)**|
|:-----|:-----|:-----|:-----|
|Single Occurrence  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Recurring Master  <br/> |**FALSE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
|Recurring Exception  <br/> |**TRUE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
   
The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**. 
  
> [!NOTE]
> The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[TaskType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

