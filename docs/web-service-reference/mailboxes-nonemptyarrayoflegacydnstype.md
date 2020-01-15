---
title: "Mailboxes (NonEmptyArrayOfLegacyDNsType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8e44bc49-8c99-472c-a507-0b5c25db9322
description: "The Mailboxes element specifies an array of mailboxes identified by legacy distinguished name."
---

# Mailboxes (NonEmptyArrayOfLegacyDNsType)

The **Mailboxes** element specifies an array of mailboxes identified by legacy distinguished name. 
  
```XML
<Mailboxes>
   <LegacyDN/>
</Mailboxes>
```

**NonEmptyArrayofLegacyDNsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[LegacyDN](legacydn.md)
  
### Parent elements

[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

