---
title: "FreeBusyAccessEnabled (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: "The FreeBusyAccessEnabled element represents the FreeBusyAccessEnabled() flag. The FreeBusyAccessEnabled element is for internal use only. This element is not used by clients."
 
 
---

# FreeBusyAccessEnabled (SOAP)

The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag. The **FreeBusyAccessEnabled** element is for internal use only. This element is not used by clients. 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 **Boolean**
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

A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization. A value of **false** indicates that the sharing relationship should be suppressed. 
  
## Remarks

Use this element to allow or suppress free/busy information from the server. 
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

