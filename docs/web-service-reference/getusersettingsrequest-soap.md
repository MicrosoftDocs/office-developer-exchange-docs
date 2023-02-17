---
title: "GetUserSettingsRequest (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: "The GetUserSettingsRequest element represents a request to retrieve specified settings for one or more users."
 
 
---

# GetUserSettingsRequest (SOAP)

The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users. 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 **GetUserSettingsRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |Represents a collection of e-mail addresses of the users for whom settings should be retrieved.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested configuration settings.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Specifies the specific server version that the provider would like to use.  <br/> |
   
### Parent elements

None.
  
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



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)

