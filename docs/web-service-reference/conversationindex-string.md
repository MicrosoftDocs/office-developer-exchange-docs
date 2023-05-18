---
title: "ConversationIndex (string)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: dda6534d-7e52-4654-b746-3631c454cb4d
description: "The ConversationIndex element specifies the location of a node in a conversation."
---

# ConversationIndex (string)

The **ConversationIndex** element specifies the location of a node in a conversation. 
  
```XML
<ConversationIndex></ConversationIndex>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationNode](conversationnode.md) <br/> |Specifies a node in a conversation.  <br/> |
   
## Text value

String value that represents the index of the conversation.
  
## Remarks

This element is required.
  
The **ConversationIndex** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

