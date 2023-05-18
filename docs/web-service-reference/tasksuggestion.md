---
title: "TaskSuggestion"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ade9ea3b-bdf1-4999-ac7d-44c6452cef36
description: "The TaskSuggestion element contains a task suggestion that resulted from an entity extracted from an item."
---

# TaskSuggestion

The **TaskSuggestion** element contains a task suggestion that resulted from an entity extracted from an item. 
  
```XML
<TaskSuggestion>
   <Position/>
   <TaskString/>
   <Assignees/>
</TaskSuggestion>
```

**TaskSuggestionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Position](position.md) | [TaskString](taskstring.md) | [Assignees](assignees.md)
  
### Parent elements

[TaskSuggestions](tasksuggestions.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

