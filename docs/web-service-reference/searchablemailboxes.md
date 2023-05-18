---
title: "SearchableMailboxes"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: eb0a7897-c642-4c93-a238-be03128af54e
description: "The SearchableMailboxes element contains an array of the mailboxes returned from a GetSearchableMailboxes request."
---

# SearchableMailboxes

The **SearchableMailboxes** element contains an array of the mailboxes returned from a **GetSearchableMailboxes** request. 
  
```XML
<SearchableMailboxes>
   <SearchableMailbox/>
</SearchableMailboxes>
```

 **ArrayOfSearchableMailboxesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[SearchableMailbox](searchablemailbox.md)
  
### Parent elements

[GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
  
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
   

