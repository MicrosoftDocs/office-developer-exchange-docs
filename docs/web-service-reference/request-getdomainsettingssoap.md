---
title: "Request (GetDomainSettings) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: "The Request element contains a request to return domain settings."
 
 
---

# Request (GetDomainSettings) (SOAP)

The **Request** element contains a request to return domain settings. 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 **GetDomainSettingsRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested configuration settings.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md) <br/> |Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.  <br/> |
   
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



[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

