---
title: "DistinguishedFolderId (DistinguishedFolderIdNameType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: "The DistinguishedFolderId element identifies folders that can be referenced by name."
---

# DistinguishedFolderId (DistinguishedFolderIdNameType)

The **DistinguishedFolderId** element identifies folders that can be referenced by name. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Specifies a generic folder.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Specifies a calendar folder.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Specifies a contacts folder.  <br/> |
   
## Text value

**DistinguishedFolderId element text values**

|**Value**|**Description**|
|:-----|:-----|
|calendar  <br/> |Indicates the URL of the calendar folder.  <br/> |
|contacts  <br/> |Indicates the URL of the contacts folder.  <br/> |
|deleteditems  <br/> |Indicates the URL of the deleted items folder.  <br/> |
|drafts  <br/> |Indicates the URL of the drafts folder.  <br/> |
|inbox  <br/> |Indicates the URL of the inbox folder.  <br/> |
|journal  <br/> |Indicates the URL of the journal folder.  <br/> |
|notes  <br/> |Indicates the URL of the notes folder.  <br/> |
|outbox  <br/> |Indicates the URL of the outbox folder.  <br/> |
|sentitems  <br/> |Indicates the URL of the sent items folder.  <br/> |
|tasks  <br/> |Indicates the URL of the tasks folder.  <br/> |
|msgfolderroot  <br/> |Indicates the URL of the message root folder.  <br/> |
|publicfoldersroot  <br/> |Indicates the URL of the public folders root folder.  <br/> |
|root  <br/> |Indicates the URL of the root folder.  <br/> |
|junkemail  <br/> |Indicates the URL of the junk email folder.  <br/> |
|searchfolders  <br/> |Indicates the URL of the search folders.  <br/> |
|voicemail  <br/> |Indicates the URL of the voice-mail folder.  <br/> |
|recoverableitemsroot  <br/> |Indicates the URL of the recoverable items root folder.  <br/> |
|recoverableitemsdeletions  <br/> |Indicates the URL of the deleted recoverable items folder.  <br/> |
|recoverableitemsversions  <br/> |Indicates the URL of the recoverable item versions folder.  <br/> |
|recoverableitemspurges  <br/> |Indicates the URL of the purged recoverable items folder.  <br/> |
|archiveroot  <br/> |Indicates the URL of the archive root folder.  <br/> |
|archivemsgfolderroot  <br/> |Indicates the URL of the archived message folder root folder.  <br/> |
|archivedeleteditems  <br/> |Indicates the URL of the archived deleted items folder.  <br/> |
|archiverecoverableitemsroot  <br/> |Indicates the URL of the archived recoverable items root folder.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Indicates the URL of the archived recoverable deleted items folder.  <br/> |
|archiverecoverableitemsversions  <br/> |Indicates the URL of the archived recoverable items versions folder.  <br/> |
|archiverecoverableitemspurges  <br/> |Indicates the URL of the archived purged recoverable items folder.  <br/> |
|syncissues  <br/> |Indicates the URL of the synchronization issues folder.  <br/> |
|conflicts  <br/> |Indicates the URL of the conflicts folder.  <br/> |
|localfailures  <br/> |Indicates the URL of the local failures folder.  <br/> |
|serverfailures  <br/> |Indicates the URL of the server failures folder.  <br/> |
|recipientcache  <br/> |Indicates the URL of the recipient cache folder.  <br/> |
|quickcontacts  <br/> |Indicates the URL of the quick contacts folder.  <br/> |
|conversationhistory  <br/> |Indicates the URL of the conversation history folder.  <br/> |
|adminauditlogs  <br/> |Indicates the URL of the administrative audit log folder.  <br/> |
|todosearch  <br/> |Indicates the URL of the search to-do folder.  <br/> |
|mycontacts  <br/> |Indicates the URL of the my contacts folder.  <br/> |
|directory  <br/> |Indicates a URL of the directory folder.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

