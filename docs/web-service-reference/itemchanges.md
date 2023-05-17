---
title: "ItemChanges"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ItemChanges
api_type:
- schema
ms.assetid: cd307892-2f69-4494-8325-219bdb5c3ad5
description: "The ItemChanges element contains an array of ItemChange elements that identify items and the updates to apply to the items."
---

# ItemChanges

The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items. 
  
[UpdateItem](updateitem.md)
  
[ItemChanges](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 **NonEmptyArrayOfItemChangesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Contains an item identifier and the updates to apply to the item.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateItem](updateitem.md) <br/> |Defines a request to update items in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/UpdateItem` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[UpdateItem operation](updateitem-operation.md)

