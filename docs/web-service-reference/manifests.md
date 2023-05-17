---
title: "Manifests"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 650d9fc0-1504-4db4-95d6-d3ba86df66ca
description: "The Manifests element contains a collection of base64-encoded app manifests that are installed for the email account."
---

# Manifests

The **Manifests** element contains a collection of base64-encoded app manifests that are installed for the email account. 
  
```XML
<Manifests>
   <Manifest/>
</Manifests>
```

 **ArrayOfAppManifestsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Manifest](manifest.md)
  
### Parent elements

[GetAppManifestsResponse](getappmanifestsresponse.md)
  
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
   

