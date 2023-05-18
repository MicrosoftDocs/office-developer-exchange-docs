---
title: "TasksFolder"
description: "The TasksFolder element represents a Tasks folder that is contained in a mailbox."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
---

# TasksFolder

The **TasksFolder** element represents a Tasks folder that is contained in a mailbox. 
  
```xml
<TasksFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</TasksFolder>
```

**TasksFolderType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a Tasks folder.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the Tasks folder.  <br/> |
|[FolderClass](folderclass.md) <br/> |Represents the folder class for a Tasks folder.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Contains the display name of a Tasks folder.  <br/> |
|[TotalCount](totalcount.md) <br/> |Represents the total count of items within a Tasks folder.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Represents the number of child folders that are contained within a Tasks folder. This property is read-only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on a Tasks folder.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contains information about a managed folder.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Represents the count of unread items within a Tasks folder.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contains all the configured permissions for a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Microsoft Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifies a single folder to create in the local client store.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifies a single folder to update in the local client store.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contains an array of folders that are used in folder operations.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element info|Value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
