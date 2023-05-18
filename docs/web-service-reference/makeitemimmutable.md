---
title: "MakeItemImmutable"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: "The MakeItemImmutable element specifies a Boolean value that indicates whether an item should be made read-only."
---

# MakeItemImmutable

The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only. 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[UpdateItemInRecoverableItems](updateiteminrecoverableitems.md)
  
## Text value

A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only. A value of **false** indicates that the item allows read-write access. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

