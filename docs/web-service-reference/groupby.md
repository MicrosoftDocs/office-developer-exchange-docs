---
title: "GroupBy"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: "The GroupBy element specifies an arbitrary grouping for FindItem queries."
---

# GroupBy

The **GroupBy** element specifies an arbitrary grouping for FindItem queries. 
  
- [FindItem](finditem.md)
- [GroupBy](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

**GroupByType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Order** <br/> | Determines the order of the groups in the grouped item array that is returned in the response. This attribute is of type SortDirectionType.  <br/> |
   
#### Order attribute values

|**Value**|**Description**|
|:-----|:-----|
|Ascending  <br/> |The groups are ordered in ascending order.  <br/> |
|Descending  <br/> |The groups are ordered in descending order.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies extended MAPI properties to get, set, or create.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Represents the field that is used to determine the order of groups in a response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/><br/> The following is the XPath expression to this element:  `/FindItem` <br/> |
   
## Remarks

The FindItem response will contain a collection of groups. Each group will contain all items that had matching values for the **GroupBy** property. The property that determines the grouping is identified in the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindItem operation](finditem-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

