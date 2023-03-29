---
title: "Disconnect (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: "The Disconnect element defines a request to disconnect a call."
---

# Disconnect (UM web service)

The **Disconnect** element defines a request to disconnect a call. 
  
- [Disconnect (UM web service)](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 **complexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CallId (UM web service)](callid-um-web-service.md) <br/> |The identifier of the call to disconnect.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Disconnect operation (UM web service)](disconnect-operation-um-web-service.md)  
- [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) 
- [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md)  
- [CallId (UM web service)](callid-um-web-service.md)

