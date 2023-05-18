---
title: "GetItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: "The GetItem element defines a request to get an item from a mailbox in the Exchange store."
---

# GetItem

The **GetItem** element defines a request to get an item from a mailbox in the Exchange store. 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 **GetItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifies the item properties and content to include in a **GetItem** response.  <br/> |
|[ItemIds](itemids.md) <br/> |Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store. These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetItem operation](getitem-operation.md)

