---
title: "Updates (Folder)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: "The Updates element contains a set of elements that define append, set, and delete changes to folder properties."
---

# Updates (Folder)

The **Updates** element contains a set of elements that define append, set, and delete changes to folder properties. 
  
- [UpdateFolder](updatefolder.md)
  
- [FolderChanges](folderchanges.md)
  
- [FolderChange](folderchange.md)
  
- [Updates (Folder)](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

**NonEmptyArrayOfFolderChangeDescriptionsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Represents data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Represents an operation to delete a given property from a folder during an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Represents a collection of changes to be performed on a single folder.  <br/> The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [UpdateFolder operation](updatefolder-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
