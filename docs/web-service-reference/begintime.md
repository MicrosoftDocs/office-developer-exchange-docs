---
title: "BeginTime"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a60c89c-9c21-4041-9593-b244ac1608ef
description: "The BeginTime element specifies the beginning of the time span to query for reminders."
---

# BeginTime

The **BeginTime** element specifies the beginning of the time span to query for reminders. 
  
```XML
<BeginTime/>
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

[GetReminders](getreminders.md)
  
## Text value

The text value of the **BeginTime** element is the beginning time of the item the reminder is for. 
  
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

