---
title: "DeleteType"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: "The DeleteType element indicates how items in a conversation are deleted."
---

# DeleteType

The **DeleteType** element indicates how items in a conversation are deleted. 
  
- [ApplyConversationAction](applyconversationaction.md)  
- [ConversationActions](conversationactions.md)  
- [ConversationAction](conversationaction.md)  
- [DeleteType](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 **DisposalType**
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

The text value of the **DeleteType** element indicates how items in a conversation are deleted. The following are the possible text values: 
  
- HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.
    
- MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.
    
- SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.
    
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ApplyConversationAction operation](applyconversationaction-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

