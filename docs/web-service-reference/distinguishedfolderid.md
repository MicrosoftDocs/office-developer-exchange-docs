---
title: "DistinguishedFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: "The DistinguishedFolderId element identifies folders that can be referenced by name. If you do not use this element, you must use the FolderId element to identify a folder."
---

# DistinguishedFolderId

The **DistinguishedFolderId** element identifies folders that can be referenced by name. If you do not use this element, you must use the [FolderId](folderid.md) element to identify a folder. 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Contains a string that identifies a default folder. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Contains a string that identifies a version of a folder that is identified by the **Id** attribute. This attribute is optional. Use this attribute to make sure that the correct version of a folder is used.  <br/> |
   
#### Id attribute values

|**Value**|**Description**|
|:-----|:-----|
|calendar  <br/> |Represents the Calendar folder.  <br/> |
|contacts  <br/> |Represents the Contacts folder.  <br/> |
|deleteditems  <br/> |Represents the Deleted Items folder.  <br/> |
|drafts  <br/> |Represents the Drafts folder.  <br/> |
|inbox  <br/> |Represents the Inbox folder.  <br/> |
|journal  <br/> |Represents the Journal folder.  <br/> |
|notes  <br/> |Represents the Notes folder.  <br/> |
|outbox  <br/> |Represents the Outbox folder.  <br/> |
|sentitems  <br/> |Represents the Sent Items folder.  <br/> |
|tasks  <br/> |Represents the Tasks folder.  <br/> |
|msgfolderroot  <br/> |Represents the message folder root.  <br/> |
|root  <br/> |Represents the root of the mailbox.  <br/> |
|junkemail  <br/> |Represents the Junk Email folder.  <br/> |
|searchfolders  <br/> |Represents the Search Folders folder.  <br/> |
|voicemail  <br/> |Represents the Voice Mail folder.  <br/> |
|recoverableitemsroot  <br/> |Represents the dumpster root folder.  <br/> |
|recoverableitemsdeletions  <br/> |Represents the dumpster deletions folder.  <br/> |
|recoverableitemsversions  <br/> |Represents the dumpster versions folder.  <br/> |
|recoverableitemspurges  <br/> |Represents the dumpster purges folder.  <br/> |
|archiveroot  <br/> |Represents the root archive folder.  <br/> |
|archivemsgfolderroot  <br/> |Represents the root archive message folder.  <br/> |
|archivedeleteditems  <br/> |Represents the archive deleted items folder.  <br/> |
|archiveinbox  <br/> |Represents the archive Inbox folder. Versions of Exchange starting with build number 15.00.0913.09 include this value.  <br/> |
|archiverecoverableitemsroot  <br/> |Represents the archive recoverable items root folder.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Represents the archive recoverable items deletions folder.  <br/> |
|archiverecoverableitemsversions  <br/> |Represents the archive recoverable items versions folder.  <br/> |
|archiverecoverableitemspurges  <br/> |Represents the archive recoverable items purges folder.  <br/> |
|syncissues  <br/> |Represents the sync issues folder.  <br/> |
|conflicts  <br/> |Represents the conflicts folder.  <br/> |
|localfailures  <br/> |Represents the local failures folder.  <br/> |
|serverfailures  <br/> |Represents the server failures folder.  <br/> |
|recipientcache  <br/> |Represents the recipient cache folder.  <br/> |
|quickcontacts  <br/> |Represents the quick contacts folder.  <br/> |
|conversationhistory  <br/> |Represents the conversation history folder.  <br/> |
|adminauditlogs  <br/> |Represents the admin audit logs folder.  <br/> |
|todosearch  <br/> |Represents the todo search folder.  <br/> |
|mycontacts  <br/> |Represents the My Contacts folder.  <br/> |
|directory  <br/> |Represents the directory folder.  <br/> |
|imcontactlist  <br/> |Represents the IM contact list folder.  <br/> |
|peopleconnect  <br/> |Represents the people connect folder.  <br/> |
|favorites  <br/> |Represents the Favorites folder.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a primary SMTP address. Proxy addresses are not allowed.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indicates the folder that is targeted for conversation actions that use folders.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indicates the destination folder for copy and move conversation actions.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifies the folder in which a new folder or item is created.  <br/><br/>The following are the XPath expressions to this element:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifies folders to search for the [FindItem operation](finditem-operation.md) and the [FindFolder operation](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Represents the collection of folders that will be searched to determine the contents of a search folder.  <br/> |
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.  <br/> |
|[FolderChange](folderchange.md) <br/> |Represents a collection of changes to be performed on a single folder.  <br/> <br/>The following is the XPath expression to this element:<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Represents the destination folder for a copied or moved item or folder.<br/><br/>The following are the XPath expressions to this element:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifies the target folder for operations that update, send, and create items in the Exchange store.<br/><br/>The following are the XPath expressions to this element:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Represents the folder that contains the items to synchronize.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Represents the name of a user configuration object. The user configuration object name is the identifier for a user configuration object.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Represents the ID of the folder that email items will be copied to.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Represents the ID of the folder that email items will be moved to.  <br/> |
   
## Text value

None.
  
## Remarks

A **DistinguishedFolderId** resolves to a **FolderId**. 
  
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
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

