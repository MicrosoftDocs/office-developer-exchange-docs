---
title: "ImItemList"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: "The ImItemList element contains a list of instant messaging groups and instant messaging contacts."
---

# ImItemList

The **ImItemList** element contains a list of instant messaging groups and instant messaging contacts. 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 **ImItemListType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [Personas](personas-ex15websvcsotherref.md)
  
#### Parent elements

[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

