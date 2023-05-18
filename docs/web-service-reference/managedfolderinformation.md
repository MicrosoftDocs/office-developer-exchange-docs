---
title: "ManagedFolderInformation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: "The ManagedFolderInformation element contains information about a managed custom folder."
---

# ManagedFolderInformation

The **ManagedFolderInformation** element contains information about a managed custom folder. 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 **ManagedFolderInformationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |Indicates whether a managed folder can be deleted by a customer.  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |Indicates whether a given managed folder can be renamed or moved by the customer.  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |Indicates whether the managed folder comment must be displayed.  <br/> |
|[HasQuota](hasquota.md) <br/> |Indicates whether the managed folder has a quota.  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |Indicates whether the managed folder is the root for all managed folders.  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |Contains the folder ID of the managed folder.  <br/> |
|[Comment](comment.md) <br/> |Contains the comment that is associated with a managed folder.  <br/> |
|[StorageQuota](storagequota.md) <br/> |Describes the storage quota for the managed folder.  <br/> |
|[FolderSize](foldersize.md) <br/> |Describes the total size of all the contents of a managed folder.  <br/> |
|[HomePage](homepage.md) <br/> |Specifies the URL that will be the default home page for the managed folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Represents a folder in the Exchange store. Managed custom folders can only be subfolders of the folder named **Managed Folders**.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Not applicable.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Not applicable.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Not applicable.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Not applicable.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[CreateManagedFolder operation](createmanagedfolder-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

