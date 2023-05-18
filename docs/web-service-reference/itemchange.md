---
title: "ItemChange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: "The ItemChange element contains an item identifier and the updates to apply to the item."
---

# ItemChange

The **ItemChange** element contains an item identifier and the updates to apply to the item. 
  
- [UpdateItem](updateitem.md) 
- [ItemChanges](itemchanges.md)
- [ItemChange](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

**ItemChangeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store. This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifies a single occurrence of a recurring item. This element is required if used. This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifies a recurrence master item by identifying one of its related occurrence items' identifiers. This element is required if used. This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.  <br/> |
|[Updates (Item)](updates-item.md) <br/> |Contains an array that defines append, set, and delete changes to item properties. This element is required.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.  <br/> The following is the XPath expression to this element:  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## Remarks

Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [UpdateItem operation](updateitem-operation.md)

