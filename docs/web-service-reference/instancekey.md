---
title: "InstanceKey"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bb4dbe9b-aea0-4527-b7d6-e928066caf38
description: "The InstanceKey element specifies an instance key for an item or conversation."
---

# InstanceKey

The **InstanceKey** element specifies an instance key for an item or conversation. 
  
```XML
<InstanceKey></InstanceKey>
```

 **base64Binary**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Represents a single conversation.  <br/> |
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
   
## Text value

The text value of the **InstanceKey** element is the instance key for an item or conversation. 
  
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

