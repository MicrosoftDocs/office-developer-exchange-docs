---
title: "PrintAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7232505a-bab0-4d78-87bc-6cc4b568937a
description: "The PrintAllowed element specifies whether printing is enabled."
---

# PrintAllowed

The **PrintAllowed** element specifies whether printing is enabled. 
  
```XML
<PrintAllowed> true | false </PrintAllowed>
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

A text value of **true** for the **PrintAllowed** element indicates that printing the contents is allowed for a rights managed item. A value of **false** indicates that printing is not allowed. 
  
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
   

