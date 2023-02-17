---
title: "TargetAutodiscoverEpr (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: "The TargetAutodiscoverEpr element represents the TargetAutodiscoverEpr property. The TargetAutodiscoverEpr element is for internal use only. This element is not used by clients."
 
 
---

# TargetAutodiscoverEpr (SOAP)

The **TargetAutodiscoverEpr** element represents the **TargetAutodiscoverEpr** property. The **TargetAutodiscoverEpr** element is for internal use only. This element is not used by clients. 
  
```XML
<TargetAutodiscoverEpr/>
```

 **anyURI**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents a list of organization relationships for a single organization.  <br/> |
   
## Text value

The text value for this element is a uniform resource identifier (URI) for the organization relationship.
  
## Remarks

This element specifies the Autodiscover URL of the server for the external organization. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
