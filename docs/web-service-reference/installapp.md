---
title: "InstallApp"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fc2ca69e-eea7-4334-b046-ec0b04d8f8c6
description: "The InstallApp element specifies the request to install an app."
---

# InstallApp

The **InstallApp** element specifies the request to install an app. 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 **InstallAppType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Manifest](manifest.md) <br/> |Contains the base64-encoded app manifest file.  <br/> |
   
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

