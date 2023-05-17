---
title: "ItemIds"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: "The ItemIds element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store."
---

# ItemIds
  
The **ItemIds** element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements. 
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifies a single occurrence of a recurring item.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Represents a single conversation.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Defines a request to delete items in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |The root element that defines a request to send items in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Defines a request to get items from the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Defines a request to move items in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Defines a request to copy items in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/CopyItem` <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteItem operation](deleteitem-operation.md)
- [SendItem operation](senditem-operation.md) 
- [GetItem operation](getitem-operation.md)
- [MoveItem operation](moveitem-operation.md)
- [CopyItem operation](copyitem-operation.md)
- [FindConversation operation](findconversation-operation.md)

