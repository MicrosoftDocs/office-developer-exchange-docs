---
title: "SetPlayOnPhoneDialString operation (UM web service)"
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
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: "The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the PlayOnPhone operation (UM web service) and the PlayOnPhoneGreeting operation (UM web service)."
 
 
---

# SetPlayOnPhoneDialString operation (UM web service)

The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).
  
## SetPlayOnPhoneDialString request example

### Description

The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## Successful SetPlayOnPhoneDialString response example

### Description

The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## See also



[SetPlayOnPhoneDialString (UM web service)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (UM web service)](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString (UM web service)](dialstring-um-web-service.md)

