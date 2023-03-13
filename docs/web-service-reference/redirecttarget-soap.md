---
title: "RedirectTarget (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: "The RedirectTarget (SOAP) element contains the target of the redirection URL or e-mail address."
 
 
---

# RedirectTarget (SOAP)

The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address. 
  
```XML
<RedirectTarget/>
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
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Represents a response to a GetUserSettings request for an individual user.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contains the requested settings for the specified domain.  <br/> |
   
## Text value

The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   

