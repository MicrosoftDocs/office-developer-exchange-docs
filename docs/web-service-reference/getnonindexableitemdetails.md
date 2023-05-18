---
title: "GetNonIndexableItemDetails"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: "The GetNonIndexableItemDetails element specifies a request to retrieve nonindexable item details."
---

# GetNonIndexableItemDetails

The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details. 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 **GetNonIndexableItemDetailsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |Specifies an array of **Mailbox** elements.  <br/> |
|[PageSize](pagesize.md) <br/> |Contains the number of items to be returned in a single page for a search result.  <br/> |
|[PageItemReference](pageitemreference.md) <br/> |Specifies the reference for a page item.  <br/> |
|[PageDirection](pagedirection.md) <br/> |Contains the direction for pagination in the search result.  <br/> |
   
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

