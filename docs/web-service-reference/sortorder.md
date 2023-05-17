---
title: "SortOrder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: "The SortOrder element defines how items are sorted in a FindItem or FindConversation request."
---

# SortOrder

The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request. 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 **NonEmptyArrayOfFieldOrdersType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldOrder](fieldorder.md) <br/> |Represents a single field by which to sort results and indicates the direction for the sort. One or more of these elements may be included. [FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> The following is the XPath expression to this element:  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Defines a request to find conversations in a mailbox.  <br/> |
   
## Text value

None.
  
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



[FindItem operation](finditem-operation.md)
  
[FindConversation operation](findconversation-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

