---
title: "MissedCallNotificationEnabled (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- MissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 8e6bf0b1-ff76-474c-ac0f-621b6ab89212
description: "The MissedCallNotificationEnabled element contains a value that indicates whether a missed call notification is enabled in a response to a GetUMProperties operation (UM web service) request."
 
 
---

# MissedCallNotificationEnabled (UM web service)

The **MissedCallNotificationEnabled** element contains a value that indicates whether a missed call notification is enabled in a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request. 
  
[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md)
  
[MissedCallNotificationEnabled (UM web service)](missedcallnotificationenabled-um-web-service.md)
  
```xml
<MissedCallNotificationEnabled/>
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
  
[SetMissedCallNotificationEnabled operation (UM web service)](setmissedcallnotificationenabled-operation-um-web-service.md)

