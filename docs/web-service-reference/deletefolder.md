---
title: "DeleteFolder"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: "The DeleteFolder element defines a request to delete folders from a mailbox in the Exchange store."
---

# DeleteFolder

The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store. 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**DeleteType** <br/> |Describes how a folder is deleted. This attribute is required.  <br/> |
   
#### DeleteType attribute

|**Value**|**Description**|
|:-----|:-----|
|HardDelete  <br/> |A folder is permanently removed from the store.  <br/> |
|SoftDelete  <br/> |A folder is moved to the dumpster if the dumpster is enabled.  <br/> |
|MoveToDeletedItems  <br/> |A folder is moved to the Deleted Items folder.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to delete.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database. This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteFolder operation](deletefolder-operation.md)

