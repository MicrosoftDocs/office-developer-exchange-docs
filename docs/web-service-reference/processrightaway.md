---
title: "ProcessRightAway"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: "The ProcessRightAway element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed. This element must be present for the response to be sent asynchronous to the requested action."
---

# ProcessRightAway

The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed. This element must be present for the response to be sent asynchronous to the requested action. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[ProcessRightAway](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 **xs:boolean**
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

A text value of **true** indicates that the response is sent as soon as the action starts processing on the server. A text value of **false** indicates that the response is sent after the action has completed. 
  
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



[ApplyConversationAction operation](applyconversationaction-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

