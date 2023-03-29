---
title: "ServerVersionInfo (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: "The ServerVersionInfo element contains the version of the server that processed the request."
 
 
---

# ServerVersionInfo (SOAP)

The **ServerVersionInfo** element contains the version of the server that processed the request. 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 **ServerVersionInfo**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MajorVersion (SOAP)](majorversion-soap.md) <br/> |The major version number for the server.  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |The minor version number for the server.  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |The major build number for the server.  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |The minor build number for the server.  <br/> |
|[Version (SOAP)](version-soap.md) <br/> |A description of the server product version.  <br/> |
   
### Parent elements

None.
  
## Remarks

This element is returned in the SOAP header.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   

