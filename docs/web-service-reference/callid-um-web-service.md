---
title: "CallId (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: "The CallId element contains the value that represents the identifier of the call in a GetCallInfo (UM web service) request or Disconnect (UM web service) request."
 
 
---

# CallId (UM web service)

The **CallId** element contains the value that represents the identifier of the call in a [GetCallInfo (UM web service)](getcallinfo-um-web-service.md) request or [Disconnect (UM web service)](disconnect-um-web-service.md) request. 
  
[GetCallInfo (UM web service)](getcallinfo-um-web-service.md)
  
[CallId (UM web service)](callid-um-web-service.md)
  
[Disconnect (UM web service)](disconnect-um-web-service.md)
  
[CallId (UM web service)](callid-um-web-service.md)
  
```xml
<CallId/>
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
|[GetCallInfo (UM web service)](getcallinfo-um-web-service.md) <br/> |Defines a request to get information about a call.  <br/> |
|[Disconnect (UM web service)](disconnect-um-web-service.md) <br/> |Defines a request to disconnect a call.  <br/> |
   
## Text value

A text value is required. The text value represents the identifier for a call.
  
## Remarks

To initial a call, use the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) or [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md). Use the text value that is returned in the [PlayOnPhoneResponse (UM web service)](playonphoneresponse-um-web-service.md) or [PlayOnPhoneGreetingResponse (UM web service)](playonphonegreetingresponse-um-web-service.md) elements for the **CallId** element text value. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md)
  
[Disconnect operation (UM web service)](disconnect-operation-um-web-service.md)
  
[PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md)

