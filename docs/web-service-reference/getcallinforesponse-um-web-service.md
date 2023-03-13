---
title: "GetCallInfoResponse (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: "The GetCallInfoResponse element defines a response to a GetCallInfo operation (UM web service) request."
 
 
---

# GetCallInfoResponse (UM web service)

The **GetCallInfoResponse** element defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request. 
  
[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMCallInfo**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|CallState  <br/> |Contains a value that indicates the status of a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.  <br/> |
|EventCause  <br/> |Contains a value that indicates the cause of an event for a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md)
  
[CallState (UM web service)](callstate-um-web-service.md)
  
[EventCause (UM web service)](eventcause-um-web-service.md)

