---
title: "AutodiscoverResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: "The AutodiscoverResponse (SOAP) element represents the base element for all responses that are returned by the Autodiscover service."
---

# AutodiscoverResponse (SOAP)

The **AutodiscoverResponse (SOAP)** element represents the base element for all responses that are returned by the Autodiscover service. 
  
- [AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 **AutodiscoverResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Represents a collection of [UserResponse (SOAP)](userresponse-soap.md) elements.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Represents a collection of [UserSettingError (SOAP)](usersettingerror-soap.md) elements.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Represents a collection of [UserSetting (SOAP)](usersetting-soap.md) elements.  <br/> |
   
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

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)
- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

