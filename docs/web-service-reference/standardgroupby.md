---
title: "StandardGroupBy"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: "The StandardGroupBy element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation."
---

# StandardGroupBy

The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation. 
  
[FindItem](finditem.md)
  
[DistinguishedGroupBy](distinguishedgroupby.md)
  
[StandardGroupBy](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 **StandardGroupByType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Provides standard groupings for FindItem queries.  <br/> |
   
## Text value

A text value is required. The only value that can be used for this element is **ConversationTopic**. **ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum). For more information about aggregation, see [AggregateOn](aggregateon.md).
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindItem operation](finditem-operation.md)
  
- [FindItem](finditem.md)

- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
