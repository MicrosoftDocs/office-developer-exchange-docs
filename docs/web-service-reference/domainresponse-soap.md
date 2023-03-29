---
title: "DomainResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: "The DomainResponse element contains the requested settings for the specified domain."
---

# DomainResponse (SOAP)

The **DomainResponse** element contains the requested settings for the specified domain. 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 **DomainResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Contains error information for settings that could not be returned.  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Identifies the target of the redirection. The target can be either a URL or an e-mail address.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Specifies the error code that is associated with the specific request.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Specifies the error message that is associated with the specific request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |Contains an array of **DomainResponse** elements. Each **DomainResponse** element contains the requested settings for the specified user.  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contains the responses for each domain.  <br/> |
   
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

