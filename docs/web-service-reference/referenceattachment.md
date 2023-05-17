---
title: "ReferenceAttachment"
 
 
ms.date: 7/7/2016
ms.audience: ITPro
ms.topic: article
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b9bde862-6b75-4a81-8033-00a47be4dc2f
description: "The ReferenceAttachment element specifies XXX."
---

# ReferenceAttachment

The **ReferenceAttachment** element specifies XXX. 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 **ReferenceAttachmen**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |The text value of the **Id** attribute is a recurring master item's unique identifier. This is a **string** value.  <br/> |
|**ChangeKey** <br/> |The text value of the **ChangeKey** attribute is the recurring master item's change key. This is a **string** value.  <br/> |
   
### Child elements

Ranges
  
### Parent elements

ItemIds | GlobalItemIds | DraftItemIds| ContactIds | GroupIds
  
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
   

