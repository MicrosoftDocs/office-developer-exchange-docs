---
title: "CopyItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: "The CopyItem element defines a request to copy an item in a mailbox in the Exchange store."
---

# CopyItem

The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store. 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 **CopyItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Represents the destination folder for a copied item.  <br/> |
|[ItemIds](itemids.md) <br/> |Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Indicates whether the item identifiers of new items are returned in the response.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[CopyItem operation](copyitem-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

