---
title: "SeekToConditionPageItemView"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: "The SeekToConditionPageItemView element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a FindItem or FindConversation search."
---

# SeekToConditionPageItemView

The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search. 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|BasePoint  <br/> |The text value of the **BasePoint** attribute is the base point from where the search will start. A text value of **Beginning** indicates that the search will start at the beginning of the result set. A text value of **End** indicates that the search will start at the end of the result set.  <br/> |
|MaxEntriesReturned  <br/> |The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.  <br/> |
   
### Child elements

[Condition (RestrictionType)](condition-restrictiontype.md)
  
### Parent elements

[FindConversation](findconversation.md) | [FindItem](finditem.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

