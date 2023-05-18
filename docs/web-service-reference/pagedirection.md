---
title: "PageDirection"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 013947f3-cf3c-40b1-baf6-405f26bd375e
description: "The PageDirection element contains the direction for pagination in the search result. The value is Previous or Next."
---

# PageDirection

The **PageDirection** element contains the direction for pagination in the search result. The value is Previous or Next. 
  
```XML
<PageDirection> Previous | Next </PageDirection>
```

 **SearchPageDirectionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SearchMailboxes](searchmailboxes.md) | [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
  
## Text value

The text value of the **PageDirection** element is the direction for pagination the search results. 
  
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
   

