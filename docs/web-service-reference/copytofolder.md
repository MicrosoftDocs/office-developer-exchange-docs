---
title: "CopyToFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CopyToFolder
api_type:
- schema
ms.assetid: 6fd8a6b8-d813-43ff-991b-0e9e782fe00e
description: "The CopyToFolder element specifies the identifier of the folder that email items can be copied to."
---

# CopyToFolder

The **CopyToFolder** element specifies the identifier of the folder that email items can be copied to. 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
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
|[Actions](actions.md) <br/> |Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[MoveToFolder](movetofolder.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

