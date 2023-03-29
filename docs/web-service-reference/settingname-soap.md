---
title: "SettingName (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: "The SettingName element represents the name of a setting in the response."
 
 
---

# SettingName (SOAP)

The **SettingName** element represents the name of a setting in the response. 
  
```XML
<SettingName/>
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
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Represents an error that is returned while retrieving a user setting.  <br/> |
|[DomainSettingError (SOAP)](domainsettingerror-soap.md) <br/> |Represents an error that occurred while retrieving a domain setting. This represents an error from a **GetDomainSettings** request.  <br/> |
   
## Text value

The value of the **SettingName** element represents the name of a setting in a response. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   

