---
title: "Users (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: "The Users element represents a collection of e-mail addresses of the users for whom settings should be retrieved."
 
 
---

# Users (SOAP)

The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved. 
  
```XML
<Users>
   <User/>
</Users>
```

 **Users**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[User (SOAP)](user-soap.md) <br/> |Represents the e-mail address of a user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |Represents a request to retrieve specified settings for one or more users.  <br/> |
|[Request (SOAP)](request-soap.md) <br/> |Contains the requested configuration settings and the target users.  <br/> |
   
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

