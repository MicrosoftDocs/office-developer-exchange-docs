---
title: "UserResponses (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: "The UserResponses element contains the configuration settings for each requested user."
 
 
---

# UserResponses (SOAP)

The **UserResponses** element contains the configuration settings for each requested user. 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 **ArrayOfUserResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Response (SOAP)](response-soap.md) <br/> |Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.  <br/> |
   
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
