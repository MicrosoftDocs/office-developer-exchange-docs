---
title: "UserResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: "The UserResponse element represents a response to a GetUserSettings request for an individual user."
 
 
---

# UserResponse (SOAP)

The **UserResponse** element represents a response to a GetUserSettings request for an individual user. 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 **UserResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Represents a message that is associated with an error code that is returned by the Autodiscover service.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Contains the target of the redirection URL or email address.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Represents a collection of information about settings that could not be returned.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |The requested settings for the user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ArrayOfUserResponse (SOAP)](arrayofuserresponse-soap.md) <br/> |Contains an array of user responses.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Contains the configuration settings for each requested user.  <br/> |
   
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

