---
title: "GetClientExtension"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c96c2b4c-45cb-482a-a3bb-7a11a0fff43b
description: "The GetClientExtension element represents a request to get a client extension."
---

# GetClientExtension

The **GetClientExtension** element represents a request to get a client extension. 
  
```XML
<GetClientExtension>
   <RequestedExtensionIds/>
   <UserParameters/>
   <IsDebug/>
</GetClientExtension>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[RequestedExtensionIds](requestedextensionids.md) | [UserParameters](userparameters.md) | [IsDebug](isdebug.md)
  
### Parent elements

None.
  
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
   

