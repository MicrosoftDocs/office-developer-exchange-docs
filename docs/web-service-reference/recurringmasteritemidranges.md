---
title: "RecurringMasterItemIdRanges"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: "The RecurringMasterItemIdRanges element specifies an array of occurrence ranges."
---

# RecurringMasterItemIdRanges

The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges. 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 **RecurringMasterItemIdRangesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |The text value of the **Id** attribute is a recurring master item's unique identifier. This is a **string** value.  <br/> |
|**ChangeKey** <br/> |The text value of the **ChangeKey** attribute is the recurring master item's change key. This is a **string** value.  <br/> |
   
### Child elements

[Ranges](ranges.md)
  
### Parent elements

[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

