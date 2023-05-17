---
title: "CreateFolderPath"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: "The CreateFolderPath element is used to create a folder path and includes a parent folder Id and a relative folder path."
---

# CreateFolderPath

The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path. 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 **CreateFolderPathType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

