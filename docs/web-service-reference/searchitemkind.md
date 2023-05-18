---
title: "SearchItemKind" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: "The SearchItemKind element indicates the type of items that are searched for a FindMailboxStatisticsByKeyword operation."
---

# SearchItemKind

The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

**SearchItemKindType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[MessageTypes](messagetypes.md)
  
## Text value

The text value of the **SearchItemKind** element is the type of item that is searched for keywords. The following list contains the text values that can be used in the **SearchItemKind** element.
  
- **Email** - Indicates that email messages are searched for keywords.
- **Meetings** - Indicates that meetings are searched for keywords.
- **Tasks** - Indicates that tasks are searched for keywords.
- **Notes** - Indicates that notes are searched for keywords.
- **Docs** - Indicates that documents are searched for keywords.
- **Journals** - Indicates that journals are searched for keywords.
- **Contacts** - Indicates that contacts are searched for keywords.
- **Im** - Indicates that instant messages are searched for keywords.
- **Voicemail** - Indicates that voice mails are searched for keywords.
- **Faxes** - Indicates that faxes are searched for keywords.
- **Posts** - Indicates that posts are searched for keywords.
- **Rssfeeds** - Indicates that RSS feeds are searched for keywords.

## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace |https://schemas.microsoft.com/exchange/services/2006/types |
|Schema name |Types schema |
|Validation file |Types.xsd |
|Can be empty ||
