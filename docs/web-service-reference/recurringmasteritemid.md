---
title: "RecurringMasterItemId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: "The RecurringMasterItemId element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items."
---

# RecurringMasterItemId

The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**OccurrenceId** <br/> |Identifies a single occurrence of a recurring master item. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Identifies a specific version of a single occurrence of a recurring master item. Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key. This attribute is optional.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contains the collection of item identifiers for all conversation items in a mailbox.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contains an item identifier and the updates to apply to the item. <br/> <br/> The following is the XPath expression to this element: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store. <br/> <br/>  The following are the XPath expressions to this element:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [OccurrenceItemId](occurrenceitemid.md)
- [FindConversation operation](findconversation-operation.md)

