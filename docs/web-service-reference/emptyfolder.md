---
title: "EmptyFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: "The EmptyFolder element defines a request to empty a folder in a mailbox in the Exchange store. Optionally, subfolders can also be deleted when the folder is emptied."
---

# EmptyFolder

The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store. Optionally, subfolders can also be deleted when the folder is emptied. 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 **EmptyFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**DeleteType** <br/> |Specifies how a folder is emptied. This attribute is required.  <br/> |
|**DeleteSubFolders** <br/> |Specifies whether subfolders are to be deleted. This attribute is required.  <br/> |
   
#### DeleteType Attribute

|**Value**|**Description**|
|:-----|:-----|
|HardDelete  <br/> |A messages and folders are permanently removed from the store.  <br/> |
|SoftDelete  <br/> |A messages and folders are moved to the dumpster if the dumpster is enabled.  <br/> |
|MoveToDeletedItems  <br/> |A messages and folders are moved to the Deleted Items folder.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to delete.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[EmptyFolder operation](emptyfolder-operation.md)

