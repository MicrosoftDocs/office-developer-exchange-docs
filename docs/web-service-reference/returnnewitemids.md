---
title: "ReturnNewItemIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: "The ReturnNewItemIds element indicates whether the item identifiers of new items are returned in the response."
---

# ReturnNewItemIds

The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response. 
  
```XML
<ReturnNewItemIds/>
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
|[CopyItem](copyitem.md) <br/> |Defines a request to copy an item in a mailbox in the Exchange store.  <br/> |
|[MoveItem](moveitem.md) <br/> |Defines a request to move an item in the Exchange store.  <br/> |
   
## Text value

A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response. A value of **false** indicates that the new item identifiers are not returned in the response. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

