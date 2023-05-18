---
title: "FolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: "The FolderId element contains the identifier and change key of a folder."
---

# FolderId

The **FolderId** element contains the identifier and change key of a folder. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Contains a string that identifies a folder in the Exchange store. This attribute is required.  <br/> |
|ChangeKey  <br/> |Contains a string that identifies a version of a folder that is identified by the Id attribute. This attribute is optional. Use this attribute to make sure that the correct version of a folder is used.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indicates the folder that is targeted for actions that use folders.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Represents an event in which an item or folder is copied.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indicates the destination folder for copy and move actions.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifies the folder where a new folder or item is created.  <br/><br/>  The following are the XPath expressions to this element:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Represents the collection of folders that will be mined to determine the contents of a search folder.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifies a single folder to delete in the local client store.  <br/> |
|[Folder](folder.md) <br/> |Represents a folder in a mailbox.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a calendar folder in a mailbox.  <br/> |
|[FolderChange](folderchange.md) <br/> |Represents a collection of changes to be performed on a single folder.  <br/> The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contact folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a task folder in a mailbox.  <br/> |
|[ToFolderId](tofolderid.md) <br/> | Represents the destination folder for a copied or moved item or folder. <br/> <br/>  The following are the XPath expressions to this element: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifies the target folder for operations that update, send, and create items in the Exchange store.  <br/><br/>  The following are the XPath expressions to this element: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Represents the folder that contains the items to synchronize.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Represents the name of a user configuration object. The user configuration object name is the identifier for a user configuration object.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifies the ID of the folder that e-mail items will be copied to.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifies the ID of the folder that e-mail items will be moved to.  <br/> |
   
## Text value

None.
  
## Remarks

All **FolderId** elements are of the **FolderIdType** type. The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice. Review the schema for more information. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

