---
title: "TaskString"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 4f2c8e66-698c-4313-98d0-24d7298489f6
description: "The TaskString element contains a suggested task."
---

# TaskString

The **TaskString** element contains a suggested task. 
  
```XML
<TaskString></TaskString>
```

**string**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[TaskSuggestion](tasksuggestion.md)
  
## Text value

The text value of the **TaskString** element is the suggested task that resulted from a task entity extracted from an item in the mailbox. 
  
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