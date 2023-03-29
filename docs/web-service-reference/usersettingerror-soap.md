---
title: "UserSettingError (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: "The UserSettingError element represents an error that is returned as a result of an attempt to get a user setting."
 
 
---

# UserSettingError (SOAP)

The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting. 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 **UserSettingError**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Respresents a message associated with an error code that is returned by the Autodiscover service.  <br/> |
|[SettingName (SOAP)](settingname-soap.md) <br/> |Represents the name of a user setting.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Represents a collection of information about settings that could not be returned.  <br/> |
   
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



[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

