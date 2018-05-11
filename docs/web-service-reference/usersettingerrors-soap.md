---
title: "UserSettingErrors (SOAP)"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: "The UserSettingErrors element represents a collection of information about settings that could not be returned."
 
 
---

# UserSettingErrors (SOAP)

The **UserSettingErrors** element represents a collection of information about settings that could not be returned. 
  
```XML
<UserSettingErrors>
    <UserSettingError/>
</UserSettingErrors>
```

 **UserSettingErrors**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Represents an error that is returned while retrieving a user setting.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Represents a response to a GetUserSettings request for an individual user.  <br/> |
   
## Text value

None.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

#### Concepts

[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

