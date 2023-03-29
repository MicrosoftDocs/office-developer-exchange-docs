---
title: "StringSetting (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bf7096d8-42d4-4bf5-bbdd-851af2754000
description: "The StringSetting element represents a user setting the value of which is of type string."
 
 
---

# StringSetting (SOAP)

The **StringSetting** element represents a user setting the value of which is of type string. 
  
```XML
<StringSetting>
   <Name/>
   <Value/>
</StringSetting>
```

 **StringSetting**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (SOAP)](name-soap.md) <br/> |Represents a user setting name.  <br/> |
|[Value (SOAP)](value-soap.md) <br/> |Represents a user setting value.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The **StringSetting** type extends the **UserSetting** type. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

