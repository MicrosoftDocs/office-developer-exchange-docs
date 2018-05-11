---
title: "GetFolder"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: "The GetFolder element defines a request to get a folder from a mailbox in the Exchange store."
---

# GetFolder

The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store. 
  
```
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 **GetFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.  <br/> |
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetFolder operation](getfolder-operation.md)

