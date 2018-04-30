---
title: "ReminderMessageData"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: "The ReminderMessageData element specifies the data in a reminder message."
---

# ReminderMessageData

The **ReminderMessageData** element specifies the data in a reminder message. 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 **ReminderMessageDataType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)
  
#### Parent elements

[Message](message-ex15websvcsotherref.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

#### Reference

[Message](message-ex15websvcsotherref.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

