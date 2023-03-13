---
title: "DomainResponses (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: "The DomainResponses element contains an array of responses for each requested domain's settings."
---

# DomainResponses (SOAP)

The **DomainResponses** element contains an array of responses for each requested domain's settings. 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 **ArrayOfDomainResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contains the requested settings for the specified domain.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.  <br/> |
|[Response (GetDomainSettings) (SOAP)](response-getdomainsettingssoap.md) <br/> |Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.  <br/> |
   
## Text value

None.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

