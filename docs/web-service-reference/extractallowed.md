---
title: "ExtractAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bc213f0e-a655-44e9-9ac9-bc1673bae1fe
description: "The ExtractAllowed element specifies whether entity extraction is enabled."
---

# ExtractAllowed

The **ExtractAllowed** element specifies whether entity extraction is enabled. 
  
```XML
<ExtractAllowed>true | false</ExtractAllowed
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
|[RightsManagementLicenseData](rightsmanagementlicensedata.md) <br/> |Specifies information about the rights management license.  <br/> |
   
## Text value

A text value of **true** for the **ExtractAllowed** element indicates that entity extraction is enabled. A value of **false** indicates that entity extraction is not enabled. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

