---
title: "SearchFilter"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: "The SearchFilter element contains the query string to filter the mailboxes to be returned from a GetSearchableMailboxes request."
---

# SearchFilter

The **SearchFilter** element contains the query string to filter the mailboxes to be returned from a **GetSearchableMailboxes** request. 
  
```XML
<SearchFilter></SearchFilter>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetSearchableMailboxes](getsearchablemailboxes.md)
  
## Text value

The text value of the **SearchFilter** element is a query string to filter mailboxes for discovery search. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

