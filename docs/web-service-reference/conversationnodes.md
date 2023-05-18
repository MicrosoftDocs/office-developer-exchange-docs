---
title: "ConversationNodes"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5c8a35b8-a940-4b3e-8768-9ba95766fd79
description: "The ConversationNodes element specifies a collection of conversation nodes."
---

# ConversationNodes

The **ConversationNodes** element specifies a collection of conversation nodes. 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 **ArrayOfConversationNodesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationNode](conversationnode.md) <br/> |Specifies a node in a conversation.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conversation (ConversationResponseType)](conversation-conversationresponsetype.md) <br/> |Represents a single conversation returned in a **GetConversationItems** response.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

