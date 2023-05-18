---
title: "Items (ArrayOfNonIndexableItemDetailsType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: da795880-12b4-4341-bcb8-31616f4ba46f
description: "The Items element contains an array of item details for non-indexable items."
---

# Items (ArrayOfNonIndexableItemDetailsType)

The **Items** element contains an array of item details for non-indexable items. 
  
```XML
<Items>
  <NonIndexableItemDetail/>
</Items>
```

 **ArrayOfNonIndexableItemDetailsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
### Parent elements

[NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[GetNonIndexableItemDetails operation](getnonindexableitemdetails-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

