---
title: "ContactsFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: "The ContactsFolder element represents a contacts folder that is contained in a mailbox."
---

# ContactsFolder

The **ContactsFolder** element represents a contacts folder that is contained in a mailbox. 
  
```xml
<ContactsFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</ContactsFolder>
```

 **ContactsFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a contacts folder.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the contacts folder.  <br/> |
|[FolderClass](folderclass.md) <br/> |Represents the folder class for a contacts folder.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Contains the display name of a contacts folder.  <br/> |
|[TotalCount](totalcount.md) <br/> |Represents the total count of items within a contacts folder.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Represents the number of child folders that are contained within a contacts folder. This property is read-only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on contacts folders.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contains information about a managed folder.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder.  <br/> |
|[SharingEffectiveRights (PermissionReadAccessType)](sharingeffectiverights-permissionreadaccesstype.md) <br/> |Indicates the permissions that the user has for the contact data that is being shared.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contains all the configured permissions for a folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifies a single folder to create in the local client store.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifies a single folder to update in the local client store.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contains an array of folders that are used in folder operations.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

