---
title: "ReplyAllAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d22f68cf-b18b-45d0-a9ff-414b7db0e67e
description: "The ReplyAllAllowed element specifies whether a reply all is allowed for rights managed data."
---

# ReplyAllAllowed

The **ReplyAllAllowed** element specifies whether a reply all is allowed for rights managed data. 
  
```XML
<ReplyAllAllowed> true | false </ReplyAllAllowed>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[RightsManagementLicenseData](rightsmanagementlicensedata.md)
  
## Text value

A text value of **true** for the **ReplyAllAllowed** element indicates that a reply all is allowed for the rights managed data. A value of **false** indicates that a reply all is not allowed. 
  
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
   

