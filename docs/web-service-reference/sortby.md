---
title: "SortBy"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: "The SortBy element contains an item property used for sorting the search result."
---

# SortBy

The **SortBy** element contains an item property used for sorting the search result. 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 **FieldOrderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Order  <br/> |The text value of the **Order** attribute is the sort order. A text value of **Ascending** indicates that the results are in ascending order. A text value of **Descending** indicates that the results are in descending order.  <br/> |
   
### Child elements

[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)
  
### Parent elements

[SearchMailboxes](searchmailboxes.md)
  
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