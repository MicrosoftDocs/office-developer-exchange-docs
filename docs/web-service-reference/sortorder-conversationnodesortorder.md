---
title: "SortOrder (ConversationNodeSortOrder)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: "The SortOrder element specifies the sort order used for the result of a GetConversationItems request."
---

# SortOrder (ConversationNodeSortOrder)

The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request. 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 **ConversationNodeSortOrder**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetConversationItems](getconversationitems.md)
  
## Text value

The text value of the **SortOrder** element is the order in which conversations ordered. A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order. A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order. A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order. A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   