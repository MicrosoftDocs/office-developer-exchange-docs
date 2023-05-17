---
title: "Updates (Item)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: "The Updates element contains a set of elements that define append, set, and delete changes to item properties."
---

# Updates (Item)

The **Updates** element contains a set of elements that define append, set, and delete changes to item properties. 
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [Updates (Item)](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

**NonEmptyArrayOfItemChangeDescriptionsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AppendToItemField](appendtoitemfield.md) <br/> |Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Contains an item identifier and the updates to apply to the item.  <br/> The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## Remarks

The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [UpdateItem operation](updateitem-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
