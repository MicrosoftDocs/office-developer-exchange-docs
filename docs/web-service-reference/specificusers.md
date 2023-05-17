---
title: "SpecificUsers"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 121b0063-5447-4063-8e54-d3fcbb8cd2be
description: "The SpecificUsers element specifies the email accounts that can access the app."
---

# SpecificUsers

The **SpecificUsers** element specifies the email accounts that can access the app. 
  
```XML
<SpecificUsers>
   <String/>
</SpecificUsers>
```

 **ArrayOfStringsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[String](string.md)
  
### Parent elements

[ClientExtension](clientextension.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

