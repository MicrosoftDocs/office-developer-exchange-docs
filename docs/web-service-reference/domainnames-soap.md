---
title: "DomainNames (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: "The DomainNames element represents the domain names collection. The DomainNames element is for internal use only. This element is not used by clients."
---

# DomainNames (SOAP)

The **DomainNames** element represents the domain names collection. The **DomainNames** element is for internal use only. This element is not used by clients. 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 **DomainNames**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents a list of organization relationships for a single organization.  <br/> |
   
## Text value

None.
  
## Remarks

This element represents the SMTP domains of the external organizations.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

