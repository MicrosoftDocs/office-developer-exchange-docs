---
title: "FoldersToIgnore"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: "The FoldersToIgnore element identifies a list of folders that are ignored when getting items in a conversation. All conversation items in the ignored folders are not returned in a GetConversationItems response."
---

# FoldersToIgnore

The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation. All conversation items in the ignored folders are not returned in a **GetConversationItems** response. 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)
  
### Parent elements

[GetConversationItems](getconversationitems.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

