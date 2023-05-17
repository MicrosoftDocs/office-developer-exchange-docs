---
title: "ReplyAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 880af57e-0fa1-473c-b87c-f02f1133ba5e
description: "The ReplyAllowed element specifies whether a reply is allowed for rights managed data."
---

# ReplyAllowed

The **ReplyAllowed** element specifies whether a reply is allowed for rights managed data. 
  
```XML
<ReplyAllowed> true | false </ReplyAllowed>
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

A text value of **true** for the **ReplyAllowed** element indicates that replies are allowed for the rights managed data. A value of **false** indicates that replies are not allowed. 
  
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
   

