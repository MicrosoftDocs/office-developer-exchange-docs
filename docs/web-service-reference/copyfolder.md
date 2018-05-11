---
title: "CopyFolder"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: 7d5cd08a-fe81-4cb6-a5a0-6dec2d3c93d4
description: "The CopyFolder element defines a request to copy folders in a mailbox in the Exchange store."
---

# CopyFolder

The **CopyFolder** element defines a request to copy folders in a mailbox in the Exchange store. 
  
```
<CopyFolder>
   <ToFolderId/>
   <FolderIds/>
</CopyFolder>
```

 **CopyFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Represents the destination folder for a copied folder.  <br/> |
|[FolderIds](folderids.md) <br/> |Contains an array of folders to copy to the folder identified by the [ToFolderId](tofolderid.md) element.  <br/> |
   
#### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[CopyFolder operation](copyfolder-operation.md)

