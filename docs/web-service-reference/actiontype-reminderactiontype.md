---
title: "ActionType (ReminderActionType)"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: "The ActionType element specifies the action to take on the reminder."
---

# ActionType (ReminderActionType)

The **ActionType** element specifies the action to take on the reminder. 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 **ReminderActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ReminderItemAction](reminderitemaction.md)
  
## Text value

The text value of the **ActionType** element specifies the action to take on the reminder. The text value of **Dismiss** indicates the reminder should be dismissed. The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[ReminderItemAction](reminderitemaction.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

