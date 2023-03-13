---
title: "Domains (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: "The Domains element represents the domain collection that is returned in a GetDomainSettings operation (SOAP), the domains that the organization has federated in a GetFederationInformation operation (SOAP), or the domains with an organization relationship as returned by GetOrganizationRelationshipSettings operation (SOAP)."
---

# Domains (SOAP)

The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **Domains**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domain (SOAP)](domain-soap.md) <br/> |Represents a single domain.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.  <br/> |
|[Response (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.  <br/> |
   
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

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

