---
title: "SetPlayOnPhoneDialString (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: "The SetPlayOnPhoneDialString element defines a request to set the default dial string for PlayOnPhone operation (UM web service) and PlayOnPhoneGreeting operation (UM web service) requests."
 
 
---

# SetPlayOnPhoneDialString (UM web service)

The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests. 
  
[SetPlayOnPhoneDialString (UM web service)](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 **complexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[dialString (UM web service)](dialstring-um-web-service.md) <br/> |The telephone number to set as the default dial string.  <br/> |
   
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



[SetPlayOnPhoneDialString operation (UM web service)](setplayonphonedialstring-operation-um-web-service.md)

