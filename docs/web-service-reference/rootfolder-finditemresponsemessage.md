---
title: "RootFolder (FindItemResponseMessage)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: "The RootFolder element contains the results of a search of a single root folder during a FindItem operation."
---

# RootFolder (FindItemResponseMessage)

The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Represents the next index that should be used for the next request when using an indexed paging view.  <br/> |
|**NumeratorOffset** <br/> |Represents the new numerator value to use for the next request when using fraction page views.  <br/> |
|**AbsoluteDenominator** <br/> |Represents the next denominator to use for the next request when doing fractional paging.  <br/> |
|**IncludesLastItemInRange** <br/> |Indicates whether the current results contain the last item in the query, such that further paging is not needed.  <br/> |
|**TotalItemsInView** <br/> |Represents the total number of items that pass the restriction. In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Items](items.md) <br/> |Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.  <br/> |
|[Groups](groups.md) <br/> |Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contains the status and result of a [FindItem operation](finditem-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[FindItem operation](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

