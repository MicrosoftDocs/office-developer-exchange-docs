---
title: "PlayOnPhoneResponse (UM web service)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 42b16880-1271-4690-abd0-0072d95b04b7
description: "The PlayOnPhoneResponse element defines a response to a PlayOnPhone operation (UM web service) request."
---

# PlayOnPhoneResponse (UM web service)

The **PlayOnPhoneResponse** element defines a response to a [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) request. 
  
[PlayOnPhoneResponse (UM web service)](playonphoneresponse-um-web-service.md)
  
```
<PlayOnPhoneResponse />
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

None.
  
## Text value

A text value is required. The text value is the call identifier to use for the value of [CallId (UM web service)](callid-um-web-service.md) in a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request or a [Disconnect operation (UM web service)](disconnect-operation-um-web-service.md) request. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md)

