---
title: "ReadFlag"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: "The ReadFlag element indicates the read state to set on items in a folder."
---

# ReadFlag

The **ReadFlag** element indicates the read state to set on items in a folder. 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[MarkAllItemsAsRead](markallitemsasread.md)
  
## Text value

A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read. A value of **false** indicates that the items in the folder will be marked as unread. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

