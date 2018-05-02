---
title: "ReminderType"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: "The ReminderType element specifies the type of reminders to return."
---

# ReminderType

The **ReminderType** element specifies the type of reminders to return. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

[GetReminders](getreminders.md)
  
## Text value

The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**. **All** is the recommended value for this element. For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetReminders](getreminders.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

