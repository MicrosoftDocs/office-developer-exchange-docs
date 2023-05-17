---
title: "ReminderItemAction"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fe67512c-5b15-4f07-8628-74cf873c2d71
description: "The ReminderItemAction element specifies the action for a reminder item."
---

# ReminderItemAction

The **ReminderItemAction** element specifies the action for a reminder item. 
  
```XML
<ReminderItemAction>
   <ActionType></ActionType>
   <ItemId></ItemId>
   <NewReminderTime></NewReminderTime>
</ReminderItemAction>
```

 **ReminderItemActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ActionType (ReminderActionType)](actiontype-reminderactiontype.md) | [ItemId](itemid.md) | [NewReminderTime](newremindertime.md)
  
### Parent elements

[ReminderItemActions](reminderitemactions.md)
  
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



[ReminderItemActions](reminderitemactions.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

