---
title: "MailboxSearchScopes"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 8b9a1979-a364-4c8f-b013-4fc04c0eeb9c
description: "The MailboxSearchScopes element specifies a list of one or more mailboxes and associated search scopes for a discovery search."
---

# MailboxSearchScopes

The **MailboxSearchScopes** element specifies a list of one or more mailboxes and associated search scopes for a discovery search. 
  
```XML
<MailboxSearchScopes>
   <MailboxSearchScope/>
<MailboxSearchScope>
```

**MailboxSearchScopeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[MailboxSearchScope](mailboxsearchscope.md)
  
### Parent elements

[MailboxQuery](mailboxquery.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

