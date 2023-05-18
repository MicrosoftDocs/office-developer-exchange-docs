---
title: "ToFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: "The ToFolderId element represents the destination folder for a copied or moved item or folder."
---

# ToFolderId

The **ToFolderId** element represents the destination folder for a copied or moved item or folder. 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

**TargetFolderIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier of a destination folder for a copied or moved item or folder.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies a named destination folder for a copied or moved item or folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |Defines a request to move a folder in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Defines a request to copy a folder in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Defines a request to move an item in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Defines a request to copy an item in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/CopyItem` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [MoveFolder operation](movefolder-operation.md)  
- [CopyFolder operation](copyfolder-operation.md) 
- [MoveItem operation](moveitem-operation.md) 
- [CopyItem operation](copyitem-operation.md)

