---
title: "ErrorCode (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: "The ErrorCode element represents an error code that is returned by the Autodiscover service."
 
 
---

# ErrorCode (SOAP)

The **ErrorCode** element represents an error code that is returned by the Autodiscover service. 
  
```XML
<ErrorCode/>
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
|[Response (SOAP)](response-soap.md) <br/> |Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Represents an error that is returned while retrieving a user setting.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.  <br/> |
   
## Text value

The text value represents the error code for an Autodiscover error response. The following table lists the possible text values for the **ErrorCode** element. 
  
|**Error code text value**|**Description**|
|:-----|:-----|
|NoError  <br/> |There was no error.  <br/> |
|RedirectAddress  <br/> |The caller must follow the e-mail address redirection that was returned by Autodiscover.  <br/> |
|RedirectUrl  <br/> |The caller must follow the URL redirection that was returned by Autodiscover.  <br/> |
|InvalidUser  <br/> |The user that was passed in the request is invalid.  <br/> |
|InvalidRequest  <br/> |The request is invalid.  <br/> |
|InvalidSetting  <br/> |A specified setting is invalid.  <br/> |
|SettingIsNotAvailable  <br/> |A specified setting is not available.  <br/> |
|ServerBusy  <br/> |The server is too busy to process the request.  <br/> |
|InvalidDomain  <br/> |The requested domain is not valid.  <br/> |
|NotFederated  <br/> |The organization is not federated.  <br/> |
|InternalServerError  <br/> |There is an internal server error.  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

