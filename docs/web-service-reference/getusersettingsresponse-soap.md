---
title: "GetUserSettingsResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: e7cd470d-5861-41e7-9e66-73ef7a59700b
description: "The GetUserSettingsResponse element represents a response to a GetUserSettings operation (SOAP) request."
 
 
---

# GetUserSettingsResponse (SOAP)

The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request. 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 **GetUserSettingsResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Represents a message that is associated with an error code that is returned by the Autodiscover service.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Contains the configuration settings for each requested user.  <br/> |
   
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

