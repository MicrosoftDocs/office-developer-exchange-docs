---
title: "DomainSettingError (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: "The DomainSettingError element represents an error that occurred while retrieving a domain setting. This represents an error from a GetDomainSettings request."
---

# DomainSettingError (SOAP)

The **DomainSettingError** element represents an error that occurred while retrieving a domain setting. This represents an error from a **GetDomainSettings** request. 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 **DomainSettingError**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Identifies the error code that is associated with the specific request.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Contains the error message that is associated with the specific request.  <br/> |
|[SettingName (SOAP)](settingname-soap.md) <br/> |Represents the name of the setting.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Contains error information for settings that could not be returned.  <br/> |
   
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

- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

