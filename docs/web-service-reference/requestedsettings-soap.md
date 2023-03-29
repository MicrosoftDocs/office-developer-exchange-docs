---
title: "RequestedSettings (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: "The RequestedSettings element contains the names of the requested configuration settings."
 
 
---

# RequestedSettings (SOAP)

The **RequestedSettings** element contains the names of the requested configuration settings. 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 **RequestedSettings**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Setting (SOAP)](setting-soap.md) <br/> |Represents a configuration setting to be returned.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |Represents a request to retrieve specified settings for one or more users.  <br/> |
|[Request (SOAP)](request-soap.md) <br/> |Contains the requested configuration settings and the target users.  <br/> |
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

