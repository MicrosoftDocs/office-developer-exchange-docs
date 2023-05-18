---
title: "Action (ConversationActionTypeType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: "The Action element contains the action to perform on the conversation specified by the ConversationId element."
---

# Action (ConversationActionTypeType)

The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element. 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Action (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contains a single action to be applied to a single conversation.  <br/> |
   
## Text value

The text value of the **Action** element indicates which action will be performed on a conversation. The following are the possible text values and the corresponding actions: 
  
- **AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element. 
    
- **AlwaysDelete** - The current items and new items in the conversation will automatically be deleted. The deletion mode is set by the [DeleteType](deletetype.md) element. 
    
- **AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element. 
    
- **Delete** - The current items in the conversation will be deleted. Subsequent items in the conversation will not be deleted. The deletion mode is set by the [DeleteType](deletetype.md) element. 
    
- **Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element. Subsequent items in the conversation will not be moved. 
    
- **Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element. Subsequent items in the conversation will not be copied. 
    
- **SetReadState** - The current items in the conversation will have their read state set. The read state is set by the [IsRead](isread.md) element. 
    
- **Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element. 
    
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
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

