---
title: "GetUserPhoto"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0e524a09-86f8-4a71-ac5c-66527ae70790
description: "The GetUserPhoto element contains the request to get a user's photo."
---

# GetUserPhoto

The **GetUserPhoto** element contains the request to get a user's photo. 
  
```XML
<GetUserPhoto>
   <Email/>
   <SizeRequested/>
</GetUserPhoto>
```

 **GetUserPhotoType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Email (String)](email-string.md) | [SizeRequested](sizerequested.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

