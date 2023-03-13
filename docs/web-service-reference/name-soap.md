---
title: "Name (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: "The Name element represents the name of a setting."
---

# Name (SOAP)

The **Name** element represents the name of a setting. 
  
```XML
<Name/>
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
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Represents a domain setting the value of which is of type string.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents a list of organization relationships for a single organization.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Represents a single user setting.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Represents a collection of server protocol connection settings.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Represents a user setting the value for which is of type string.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Represents a user setting that is a collection of Exchange Web client URLs.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Contains a collection of alternate mailbox settings.  <br/> |
   
## Text value

The text value of the **Name** element is the name of a setting. 
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)
- [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

