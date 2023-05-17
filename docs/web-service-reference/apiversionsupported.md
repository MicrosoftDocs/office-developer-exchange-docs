---
title: "ApiVersionSupported"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d9264e74-eba7-4279-b193-af7e5130268d
description: "The ApiVersionSupported element contains the version of the JavaScript API for Office supported by the client."
---

# ApiVersionSupported

The **ApiVersionSupported** element contains the version of the JavaScript API for Office supported by the client. 
  
```XML
<ApiVersionSupported />
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetAppManifests](getappmanifests.md)
  
## Text value

The text value of the **ApiVersionSupported** element contains the version of the JavaScript API for Office supported by the client. This value indicates which app manifests should be returned to the client in the response. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetAppManifests](getappmanifests.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

