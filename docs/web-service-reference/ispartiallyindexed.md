---
title: "IsPartiallyIndexed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 542e7b90-eafe-4711-a9d7-71bbc30d9646
description: "The IsPartiallyIndexed element indicates whether the item is partially indexed."
---

# IsPartiallyIndexed

The **IsPartiallyIndexed** element indicates whether the item is partially indexed. 
  
```XML
<IsPartiallyIndexed>true | false</IsPartiallyIndexed>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## Text value

A text value of **true** for the **IsPartiallyIndexed** element indicates that the mailbox item is partially indexed. A value of **false** indicates that the mailbox item is not partially indexed. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

