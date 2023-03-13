---
title: "PlayOnPhoneGreeting (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: "The PlayOnPhoneGreeting element defines a request to play a Unified Messaging greeting on a telephone."
 
 
---

# PlayOnPhoneGreeting (UM web service)

The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone. 
  
[PlayOnPhoneGreeting (UM web service)](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 **complexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[GreetingType (UM web service)](greetingtype-um-web-service.md) <br/> |Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.  <br/> |
|[dialString (UM web service)](dialstring-um-web-service.md) <br/> |Contains the value for the telephone number to dial.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md)

