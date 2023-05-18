---
title: "GetHoldOnMailboxes"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 4c94cfb7-42e2-42e4-9c6d-a1b0f4747f83
description: "The GetHoldOnMailboxes element indicates the beginning of the GetHoldOnMailboxes request."
---

# GetHoldOnMailboxes

The **GetHoldOnMailboxes** element indicates the beginning of the **GetHoldOnMailboxes** request. 
  
```XML
<GetHoldOnMailboxes>
   <HoldId/>
</GetHoldOnMailboxes>
```

 **GetHoldOnMailboxesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[HoldId](holdid.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

