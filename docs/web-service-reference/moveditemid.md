---
title: "MovedItemId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: "The MovedItemId element specifies the identifier of the item that was moved by the MarkAsJunk operation."
---

# MovedItemId

The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation. 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation. The item identifier will remain the same after the move.  <br/> |
|ChangeKey  <br/> |The value of the **ChangeKey** attribute is the change key of the moved item. The change key changes after the item is moved by the **MarkAsJunk** operation.  <br/> |
   
### Child elements

None.
  
### Parent elements

[MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

