---
title: "FieldOrder"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldOrder
api_type:
- schema
ms.assetid: b9364842-bbe2-4221-afef-bf5022bc89ec
description: "The FieldOrder element represents a single field by which to sort results and indicates the direction for the sort."
---

# FieldOrder

The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort. 
  
```
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

 **FieldOrderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Order** <br/> | Describes the sort order direction. The following are the possible values:  <br/>  Ascending  <br/>  Descending  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SortOrder](sortorder.md) <br/> |Defines how items are sorted in a FindItem request.  <br/> The following is the XPath expression to this element:  `/FindItem/SortOrder` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

