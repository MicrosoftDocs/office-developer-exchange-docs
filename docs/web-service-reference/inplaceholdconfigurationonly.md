---
title: "InPlaceHoldConfigurationOnly"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 921ecc73-b7e2-40a7-8458-68f18dd5a13b
description: "The InPlaceHoldConfigurationOnly element specifies whether to include the in-place hold configuration."
---

# InPlaceHoldConfigurationOnly

The **InPlaceHoldConfigurationOnly** element specifies whether to include the in-place hold configuration. 
  
```XML
<InPlaceHoldConfigurationOnly>true | false</InPlaceHoldConfigurationOnly>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
  
## Text value

A text value of **true** for the **InPlaceHoldConfigurationOnly** element indicates that the in-place hold configuration is included. A value of **false** indicates that the in-place hold configuration is not included. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

