---
title: "RecurringMasterItemId (ItemIdType)"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: "The RecurringMasterItemId (ItemIdType) element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items."
---

# RecurringMasterItemId (ItemIdType)

The **RecurringMasterItemId (ItemIdType)** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items. 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

****

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Identifies a single occurrence of a recurring master item. This attribute is required.  <br/> |
|ChangeKey  <br/> |Identifies a specific version of a single occurrence of a recurring master item. Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key. This attribute is optional.  <br/> |
   
### Child elements

None.
  
### Parent elements

[Reminder](reminder.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Reminder](reminder.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

