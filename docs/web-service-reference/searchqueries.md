---
title: "SearchQueries"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 67328dab-321b-45ad-929e-cd83e65ad87e
description: "The SearchQueries element contains a list of mailboxes and associated queries for discovery search."
---

# SearchQueries

The **SearchQueries** element contains a list of mailboxes and associated queries for discovery search. 
  
```XML
<SearchQueries>
   <MailboxQuery/>
</SearchQueries>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[MailboxQuery](mailboxquery.md)
  
### Parent elements

[SearchMailboxes](searchmailboxes.md) | [SearchMailboxesResult](searchmailboxesresult.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

