---
title: "FolderChanges"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: "The FolderChanges element represents a collection of changes for a folder."
---

# FolderChanges

The **FolderChanges** element represents a collection of changes for a folder. 
  
[UpdateFolder](updatefolder.md)
  
[FolderChanges](folderchanges.md)
  
```
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 **NonEmptyArrayOfFolderChangesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Represents a single change to be performed on a single folder.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateFolder](updatefolder.md) <br/> |Represents the operation that is used to update properties for a folder.  <br/> The following is the XPath expression to this element:  <br/>  `/UpdateFolder` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[UpdateFolder operation](updatefolder-operation.md)

