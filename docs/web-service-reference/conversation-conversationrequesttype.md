---
title: "Conversation (ConversationRequestType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: "Represents a single conversation returned in a GetConversationItems response."
---

# Conversation (ConversationRequestType)

The **Conversation** element represents a single conversation returned in a **GetConversationItems** response. 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)
  
### Parent elements

[Conversations](conversations-ex15websvcsotherref.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

