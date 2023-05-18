---
title: "Deduplication"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: "The Deduplication element indicates whether the search result should remove duplicate items."
---

# Deduplication

The **Deduplication** element indicates whether the search result should remove duplicate items. 
  
```XML
<Deduplication> true | false </Deduplication>
```

**Boolean**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)
  
## Text value

A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items. A value of **false** indicates that search results may contain duplicate items. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

