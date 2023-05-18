---
title: "HasChanged"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: "The HasChanged element indicates whether a user's photo has changed."
---

# HasChanged

The **HasChanged** element indicates whether a user's photo has changed. 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetUserPhotoResponse](getuserphotoresponse.md)
  
## Text value

A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned. A value of **false** indicates that the photo has not changed since the last time it was returned. 
  
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
   

