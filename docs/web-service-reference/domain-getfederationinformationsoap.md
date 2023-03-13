---
title: "Domain (GetFederationInformation) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 56aeb659-8309-47a6-8c41-9f8b0436438c
description: "The Domain element identifies the domain that has a federation trust."
---

# Domain (GetFederationInformation) (SOAP)

The **Domain** element identifies the domain that has a federation trust. 
  
```XML
<Domain/>
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
|[Request (GetFederationInformation) (SOAP)](request-getfederationinformationsoap.md) <br/> |Represents a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.  <br/> |
   
## Text value

The text value represents the domain name of the domain that contains the federation trust.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

