---
title: "GlobalHasIrm"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: "The GlobalHasIrm element specifies whether at least one message in the conversation and across all folders is an IRM protected message."
---

# GlobalHasIrm

The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message. 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Conversation (ConversationType)](conversation-conversationtype.md)
  
## Text value

The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message. Otherwise the value is **false**.
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Conversation (ConversationType)](conversation-conversationtype.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

