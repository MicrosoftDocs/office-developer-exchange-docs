---
title: "CallState (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: "The CallState element contains a value that indicates the status of a call."
 
 
---

# CallState (UM web service)

The **CallState** element contains a value that indicates the status of a call. 
  
[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md)
  
[CallState (UM web service)](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md) <br/> |Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).  <br/> |
   
## Text value

A text value is required. The following are the possible values:
  
- Idle
    
- Connecting
    
- Alerted
    
- Connected
    
- Disconnected
    
- Incoming
    
- Transferring
    
- Forwarding
    
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md)

