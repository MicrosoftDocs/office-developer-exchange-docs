---
title: "IsWritable"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: "The IsWritable element specifies whether the underlying contact or Active Directory recipient can be written to."
---

# IsWritable

The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to. 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## Text value

A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access. A value of **false** indicates that the contact or Active Directory object is not available for write access. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  

