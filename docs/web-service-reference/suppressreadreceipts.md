---
title: "SuppressReadReceipts"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: "The SuppressReadReceipts element indicates whether read receipts should be suppressed."
---

# SuppressReadReceipts

The **SuppressReadReceipts** element indicates whether read receipts should be suppressed. 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)
  
## Text value

A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed. A value of **false** indicates that read receipts will be sent to the sender. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

