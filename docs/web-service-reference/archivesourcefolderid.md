---
title: "ArchiveSourceFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d5b6a099-3b87-44ef-a197-8198730ff72d
description: "The ArchiveSourceFolderId element specifies the Id of the source folder for the archive item."
---

# ArchiveSourceFolderId

The **ArchiveSourceFolderId** element specifies the Id of the source folder for the archive item. 
  
```XML
<ArchiveSourceFolderId>
   <FolderId/>
   <DistinguishedFolderId/>
   <AddressListId/>
</ArchiveSourceFolderId>
```

 **TargetFolderIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md) | [AddressListId](addresslistid.md)
  
### Parent elements

[ArchiveItem](archiveitem.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

