---
title: "OofStatus (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: "The OofStatus element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a GetUMProperties operation (UM web service) request."
 
 
---

# OofStatus (UM web service)

The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request. 
  
[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (UM web service)](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md) <br/> |Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.  <br/> |
   
## Text value

A Boolean text value is required. The following are the possible values:
  
- True
    
- False
    
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md)

