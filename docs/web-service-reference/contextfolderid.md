---
title: "ContextFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: "The ContextFolderId element indicates the folder that is targeted for actions that use folders. This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder."
---

# ContextFolderId

The **ContextFolderId** element indicates the folder that is targeted for actions that use folders. This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder. 
  
- [ApplyConversationAction](applyconversationaction.md) 
- [ConversationActions](conversationactions.md)
- [ConversationAction](conversationaction.md)
- [ContextFolderId](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


**TargetFolderIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of the context folder.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies folders that can be referenced by name.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contains a single action to be applied to a single conversation.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ApplyConversationAction operation](applyconversationaction-operation.md)

