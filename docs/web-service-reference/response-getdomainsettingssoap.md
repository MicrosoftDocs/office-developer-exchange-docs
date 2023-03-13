---
title: "Response (GetDomainSettings) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: "The Response element represents the response to a GetDomainSettings call for an individual domain."
 
 
---

# Response (GetDomainSettings) (SOAP)

The **Response** element represents the response to a **GetDomainSettings** call for an individual domain. 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 **GetDomainSettingsResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contains the response for each domain requested in a **GetDomainSettings** request.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Contains the error code that is associated with the response, if applicable.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Contains the error message that is associated with the response, if applicable.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |Returns to the caller the domain configuration settings.  <br/> |
   
## Text value

None.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

