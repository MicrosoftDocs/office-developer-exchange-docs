---
title: "MailboxSearchScope"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ef4a4203-61e5-46b8-9fa4-d1a10e785aa2
description: "The MailboxSearchScope element specifies a mailbox and a search scope for a discovery search."
---

# MailboxSearchScope

The **MailboxSearchScope** element specifies a mailbox and a search scope for a discovery search. 
  
```XML
<MailboxSearchScope>
   <Mailbox/>
   <SearchScope/>
<MailboxSearchScope>
```

**MailboxSearchScopeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Mailbox (string)](mailbox-string.md) | [SearchScope](searchscope.md)
  
### Parent elements

[MailboxSearchScopes](mailboxsearchscopes.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

