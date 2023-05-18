---
title: "ImListMigrationCompleted"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: "The ImListMigrationCompleted element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients."
---

# ImListMigrationCompleted

The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients. 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetImListMigrationCompleted](setimlistmigrationcompleted.md)
  
## Text value

A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store. A value of **false** indicates that the instant message contacts store has not been migrated. 
  
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
   

