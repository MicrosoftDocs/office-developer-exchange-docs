---
title: "FreeBusyAccessLevel (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: "The FreeBusyAccessLevel element represents the FreeBusyAccessLevel property. The FreeBusyAccessLevel element is for internal use only. This element is not used by clients."
 
 
---

# FreeBusyAccessLevel (SOAP)

The **FreeBusyAccessLevel** element represents the **FreeBusyAccessLevel** property. The **FreeBusyAccessLevel** element is for internal use only. This element is not used by clients. 
  
```XML
<FreeBusyAccessLevel/>
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
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents a list of organization relationships for a single organization.  <br/> |
   
## Remarks

This element specifies the maximum amount of free/busy detail that will be returned in the response and indicates the level of free/busy data that is externally shared. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

