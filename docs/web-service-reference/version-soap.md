---
title: "Version (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 47c9216e-6bfe-48c8-a27a-26f70db8e8d5
description: "The Version element represents a description of the server product version."
 
 
---

# Version (SOAP)

The **Version** element represents a description of the server product version. 
  
```XML
<Version/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Contains the version of the server that processed the request.  <br/> |
   
## Text value

The value of the **Version** element is a description of the server product version. 
  
## Remarks

The **Version** element is contained in the SOAP header of a response. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

