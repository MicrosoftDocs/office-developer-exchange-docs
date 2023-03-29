---
title: "ErrorMessage (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: "The ErrorMessage element represents a message that is associated with an error code that is returned by the Autodiscover service."
 
 
---

# ErrorMessage (SOAP)

The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service. 
  
```XML
<ErrorMessage/>
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
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |Represents the base type for all responses that are returned by the Autodiscover service.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contains the requested settings for the specified domain.  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.  <br/> |
|[Response (SOAP)](response-soap.md) <br/> |Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Represents an error that is returned while retrieving a user setting.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.  <br/> |
   
## Text value

The text value represents the error message.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

