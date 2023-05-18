---
title: "OccurrenceItemId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: "The OccurrenceItemId element identifies a single occurrence of a recurring item."
---

# OccurrenceItemId

The **OccurrenceItemId** element identifies a single occurrence of a recurring item. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Identifies the recurring master of a recurring item. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Identifies a specific version of the recurring master or an item occurrence. If either the recurring master or any of its occurrences change, the **ChangeKey** changes. The **ChangeKey** is the same for the recurring master and all occurrences.  <br/> |
|**InstanceIndex** <br/> |Identifies the index of the item occurrence. This attribute is required. This value represents an integer.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contains the collection of item identifiers for all conversation items in a mailbox.  <br/> |
|[ItemIds](itemids.md) <br/> | Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store. <br/><br/>The following are the XPath expressions to this element: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**NOTE**: [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items. Item occurrences are invalid with these operations.           |
|[ItemChange](itemchange.md) <br/> |Contains an item identifier and the updates to apply to the item.<br/><br/> The following is the XPath expression to this element:  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [RecurringMasterItemId](recurringmasteritemid.md)
- [FindConversation operation](findconversation-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

