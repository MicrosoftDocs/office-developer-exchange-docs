---
title: "Range"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: "The Range element specifies a range of calendar item occurrences for a repeating calendar item."
---

# Range

The **Range** element specifies a range of calendar item occurrences for a repeating calendar item. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Start** <br/> |The text value of the **Start** attribute is the start date of the recurring item range. This is a **dateTime** value.  <br/> |
|**End** <br/> |The text value of the **End** attribute is the end date of the recurring item range. This is a **dateTime** value.  <br/> |
|**Count** <br/> |The text value of the **Count** attribute is the number of occurrences of the recurring item. This is an **integer** value.  <br/> |
|**CompareOriginalStartTime** <br/> |The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time. A value of **false** indicates that the client does not need to compare the original start time with the new start time.  <br/> |
   
### Child elements

None.
  
### Parent elements

[Ranges](ranges.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

