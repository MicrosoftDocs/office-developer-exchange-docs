---
title: "Folders"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: "The Folders element contains an array of folders that are used in folder operations."
---

# Folders

The **Folders** element contains an array of folders that are used in folder operations. 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Identifies a folder to create, get, find, synchronize, or update.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a folder that primarily contains calendar items.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a Contacts folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a Search folder contained in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a Tasks folder in a mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.  <br/> |
|[CreateFolder](createfolder.md) <br/> |Defines a request to create a folder in the Exchange store.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifies the folder where a new folder is created.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.  <br/> |
   
## Remarks

This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)
