---
title: "MarkAllItemsAsReadResponseMessage"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e52f56d4-c6a3-458a-8abb-4e0c19d32341
description: "The MarkAllItemsAsReadResponseMessage element specifies the response message for a MarkAllItemsAsRead request."
---

# MarkAllItemsAsReadResponseMessage

The **MarkAllItemsAsReadResponseMessage** element specifies the response message for a **MarkAllItemsAsRead** request. 
  
```XML
<MarkAllItemsAsReadResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</MarkAllItemsAsReadResponseMessage>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md)
  
### Parent elements

[ResponseMessages](responsemessages.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

