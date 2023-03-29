---
title: "OrganizationRelationshipSettingsCollection (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 33456abf-a1b6-46da-a864-3ec8af2780de
description: "The OrganizationRelationshipSettingsCollection element represents a list of organization relationships that match the query. The OrganizationRelationshipSettingsCollection element is for internal use only. This element is not used by clients."
 
 
---

# OrganizationRelationshipSettingsCollection (SOAP)

The **OrganizationRelationshipSettingsCollection** element represents a list of organization relationships that match the query. The **OrganizationRelationshipSettingsCollection** element is for internal use only. This element is not used by clients. 
  
```XML
<OrganizationRelationshipSettingsCollection>
   <OrganizationRelationshipSettings/>
</OrganizationRelationshipSettingsCollection>
```

 **OrganizationRelationshipSettingsCollection**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents the list of organization relationships for the selected organization and SMTP addresses.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Response (GetOrganizationRelationship) (SOAP)](response-getorganizationrelationshipsoap.md) <br/> |Contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.  <br/> |
   
## Text value

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

[GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)