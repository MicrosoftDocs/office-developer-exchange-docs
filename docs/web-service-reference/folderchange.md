---
title: "FolderChange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: "The FolderChange element represents a collection of changes to be performed on a single folder."
---

# FolderChange

The **FolderChange** element represents a collection of changes to be performed on a single folder. 
  
- [UpdateFolder](updatefolder.md) 
- [FolderChanges](folderchanges.md) 
- [FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

**FolderChangeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder to update.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.  <br/> |
|[Updates (Folder)](updates-folder.md) <br/> |Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Represents a collection of changes for a folder.  <br/> The following is the XPath expression to this element:  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [UpdateFolder operation](updatefolder-operation.md)

