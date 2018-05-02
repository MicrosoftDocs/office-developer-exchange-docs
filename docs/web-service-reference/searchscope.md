---
title: "SearchScope"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: "The SearchScope element specifies the scope of a search."
---

# SearchScope

The **SearchScope** element specifies the scope of a search. 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 **MailboxSearchLocationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

[MailboxSearchScope](mailboxsearchscope.md)
  
## Text value

The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search. A text value of **PrimaryOnly** indicates that the primary mailbox is searched. A text value of **ArchiveOnly** indicates that the archive mailbox is searched. A text value of **All** indicates that both the primary and archive mailboxes are searched. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

