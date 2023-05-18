---
title: "ConversationNode"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: "The ConversationNode element specifies a node in a conversation."
---

# ConversationNode

The **ConversationNode** element specifies a node in a conversation. 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 **ConversationNodeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[InternetMessageId](internetmessageid.md) <br/> |Represents the Internet message identifier of an item.  <br/> |
|[ParentInternetMessageId](parentinternetmessageid.md) <br/> |Specifies the identifier of the parent Internet message.  <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |Specifies all the items in the conversation node.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationNodes](conversationnodes.md) <br/> |Specifies a collection of conversation nodes.  <br/> |
   
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

