---
title: "Manifest"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: af0d7435-fef6-4f0d-bd22-00e3fa576315
description: "The Manifest element contains the base64-encoded app manifest file."
---

# Manifest

The **Manifest** element contains the base64-encoded app manifest file. 
  
```XML
<Manifest></Manifest>
```

 **base64Binary**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Manifests](manifests.md) | [InstallApp](installapp.md) | [ClientExtension](clientextension.md)
  
## Text value

The text value of the Manifest element is an ASCII representation of the base64 binary encoded form of the client app manifest file.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  

