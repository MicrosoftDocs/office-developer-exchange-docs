---
title: "ArrayOfUserResponse (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 3e5cf65c-8d0b-4fd9-8207-56c07f914acd
description: "The ArrayOfUserResponse element contains an array of UserResponse (SOAP) elements."
---

# ArrayOfUserResponse (SOAP)

The **ArrayOfUserResponse** element contains an array of [UserResponse (SOAP)](userresponse-soap.md) elements. 
  
```XML
<ArrayOfUserResponse>
   <UserResponse/>
</ArrayOfUserResponse>
```

 **ArrayOfUserResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Contains the requested settings for the specified user.  <br/> |
   
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

