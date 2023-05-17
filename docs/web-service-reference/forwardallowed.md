---
title: "ForwardAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bc32e0f4-61e9-4c9f-9a03-90a07eb51c53
description: "The ForwardAllowed element specifies whether forwarding emails is enabled."
---

# ForwardAllowed

The **ForwardAllowed** element specifies whether forwarding emails is enabled. 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
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

A text value of **true** for the **ForwardAllowed** element indicates that forwarding emails is allowed. A value of **false** indicates that forwarding is not allowed. 
  
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

