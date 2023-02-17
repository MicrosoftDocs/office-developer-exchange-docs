---
title: "GetDomainSettingsRequest (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: "The GetDomainSettingsRequest element represents a GetDomainSettings operation (SOAP) operation request."
 
 
---

# GetDomainSettingsRequest (SOAP)

The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request. 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 **GetDomainSettingsRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Represents a collection of domain identifiers.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested domain configuration settings.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Specifies the server version that the provider will use.  <br/> |
   
### Parent elements

None.
  
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

