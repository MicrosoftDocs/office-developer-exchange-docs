---
title: "dialString (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- dialString
api_type:
- schema
ms.assetid: d1e3cd23-48fe-4ebc-a5c5-2226d223f800
description: "The dialString element contains the value for the telephone number to dial."
---

# dialString (UM web service)

The **dialString** element contains the value for the telephone number to dial. 
  
- [PlayOnPhone (UM web service)](playonphone-um-web-service.md) 
- [dialString (UM web service)](dialstring-um-web-service.md) 
- [PlayOnPhoneGreeting (UM web service)](playonphonegreeting-um-web-service.md) 
- [dialString (UM web service)](dialstring-um-web-service.md)
  
```xml
<dialString/>
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
|[PlayOnPhone (UM web service)](playonphone-um-web-service.md) <br/> |Defines a request to play a message on a telephone.  <br/> |
|[PlayOnPhoneGreeting (UM web service)](playonphonegreeting-um-web-service.md) <br/> |Defines a request to play a greeting on a telephone.  <br/> |
   
## Text value

A text value is required. The text value must contain a valid dialing number.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [PlayOnPhone (UM web service)](playonphone-um-web-service.md)  
- [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md)  
- [PlayOnPhoneGreeting (UM web service)](playonphonegreeting-um-web-service.md)  
- [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md)

