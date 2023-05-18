---
title: "ReminderItemActions"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 135d7fc3-7d5b-4e30-9a6f-62eb02d7ab98
description: "The ReminderItemActions element specifies the actions for reminder items."
---

# ReminderItemActions

The **ReminderItemActions** element specifies the actions for reminder items. 
  
```XML
<ReminderItemActions>
   <ReminderItemAction></ReminderItemAction>
</ReminderItemActions>
```

 **NonEmptyArrayOfReminderItemActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ReminderItemAction](reminderitemaction.md)
  
### Parent elements

[PerformReminderAction](performreminderaction.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[PerformReminderAction](performreminderaction.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

