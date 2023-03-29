---
title: "EventCause (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: "The EventCause element contains a value that indicates the cause for a call event in a response to a GetCallInfo operation (UM web service) request."
 
 
---

# EventCause (UM web service)

The **EventCause** element contains a value that indicates the cause for a call event in a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request. 
  
[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md)
  
[EventCause (UM web service)](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md) <br/> |Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.  <br/> |
   
## Text value

A text value is required. The following are the possible values:
  
- None
    
- UserBusy
    
- NoAnswer
    
- Other
    
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (UM web service)](getcallinforesponse-um-web-service.md)

