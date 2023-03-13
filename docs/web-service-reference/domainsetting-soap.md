---
title: "DomainSetting (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: "The DomainSetting element contains domain settings that are returned by the GetDomainSettings operation (SOAP) operation request."
---

# DomainSetting (SOAP)

The **DomainSetting** element contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request. 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 **DomainSetting**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (SOAP)](name-soap.md) <br/> |Represents the name of a setting.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.  <br/> |
   
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

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

