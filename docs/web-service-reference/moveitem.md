---
title: "MoveItem"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: "The MoveItem element defines a request to move an item in the Exchange store."
---

# MoveItem

The **MoveItem** element defines a request to move an item in the Exchange store. 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 **MoveItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Represents the destination folder for a moved item.  <br/> |
|[ItemIds](itemids.md) <br/> |Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Indicates whether the item identifiers of new items are returned in the response.  <br/> |
   
#### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[MoveItem operation](moveitem-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

