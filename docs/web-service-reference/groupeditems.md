---
title: "GroupedItems"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupedItems
api_type:
- schema
ms.assetid: 53170df4-4272-4b37-b23f-cd8e2d4a7396
description: "The GroupedItems element represents a collection of items that are the result of a grouped FindItem operation call."
---

# GroupedItems

The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call. 
  
[FindItemResponse](finditemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[FindItemResponseMessage](finditemresponsemessage.md)
  
[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
  
[Groups](groups.md)
  
[GroupedItems](groupeditems.md)
  
```
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 **GroupedItemsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[GroupIndex](groupindex.md) <br/> |Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.  <br/> |
|[Items](items.md) <br/> |Contains an array of grouped items.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Groups](groups.md) <br/> |Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[FindItem operation](finditem-operation.md)
#### Other resources

[Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

