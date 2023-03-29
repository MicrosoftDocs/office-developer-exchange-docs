---
title: "ArrayOfDomainResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6dbd9221-e019-4981-bcdb-ea370331f407
description: "The ArrayOfDomainResponse element contains an array of responses for each requested domain's settings."
---

# ArrayOfDomainResponse (SOAP)

The **ArrayOfDomainResponse** element contains an array of responses for each requested domain's settings. 
  
```XML
<ArrayOfDomainResponse>
   <DomainResponse/>
</ArrayOfDomainResponse>
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

None.
  
## Text value

None.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

