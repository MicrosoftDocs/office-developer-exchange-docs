---
title: "Update (FolderSync)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: "The Update element identifies a single folder to update in the local client store."
---

# Update (FolderSync)

The **Update** element identifies a single folder to update in the local client store. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Changes (Hierarchy)](changes-hierarchy.md)
  
[Update (FolderSync)](update-foldersync.md)
  
```
<Update>
   <Folder/>
</Update>
```

 **SyncFolderHierarchyCreateOrUpdateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Defines the folder to create, get, find, synchronize, or update.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a folder that primarily contains calendar items.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contact folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder that is contained in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a task folder t is thcontained in a mailbox.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Changes (Hierarchy)](changes-hierarchy.md) <br/> |Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[SyncFolderItems operation](syncfolderitems-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

