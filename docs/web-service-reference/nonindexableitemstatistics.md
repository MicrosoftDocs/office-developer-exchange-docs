---
title: "NonIndexableItemStatistics"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: "The NonIndexableItemStatistics element contains an array of statistics for items that could not be indexed."
---

# NonIndexableItemStatistics

The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed. 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 **ArrayOfNonIndexableItemStatisticsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

[NonIndexableItemStatistic](nonindexableitemstatistic.md)
  
#### Parent elements

[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetNonIndexableItemStatistics operation](getnonindexableitemstatistics-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

