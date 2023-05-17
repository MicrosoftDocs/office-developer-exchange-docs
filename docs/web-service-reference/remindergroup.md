---
title: "ReminderGroup"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: "The ReminderGroup element specifies whether the reminder is for a calendar item or a task."
---

# ReminderGroup

The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task. 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 **ReminderGroupType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Reminder](reminder.md)
  
## Text value

The text value of the **ReminderGroup** element is the group type of the reminder. The text value of **Calendar** specifies that the reminder is for a calendar item. The text value of **Task** specifies that the reminder is for a task item. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Reminder](reminder.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)