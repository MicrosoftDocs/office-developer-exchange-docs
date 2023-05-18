---
title: "HasAttachment"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: "The HasAttachment element specifies a Boolean value to indicate whether the item has attachments."
---

# HasAttachment

The **HasAttachment** element specifies a Boolean value to indicate whether the item has attachments. 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchPreviewItem](searchpreviewitem.md) <br/> |Specifies the first 256 characters of a mailbox item for preview without opening the item.  <br/> |
   
## Text value

A text value of **true** for the **HasAttachment** element indicates that the item has an attachment. A value of **false** indicates that the item does not have an attachment. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

