---
title: "PlayOnPhoneGreeting operation (UM web service)"
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
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: "The PlayOnPhoneGreeting operation makes an outbound call and plays one of the two greeting messages on the telephone."
 
 
---

# PlayOnPhoneGreeting operation (UM web service)

The PlayOnPhoneGreeting operation makes an outbound call and plays one of the two greeting messages on the telephone.
  
## PlayOnPhoneGreeting request example

### Description

The following example of a PlayOnPhoneGreeting request shows how to form a request to make an outbound call and play the normal greeting message on a telephone.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## Successful PlayOnPhoneGreeting response example

### Description

The following example of a PlayOnPhoneGreeting response shows a response to the PlayOnPhoneGreeting request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## See also



[PlayOnPhoneGreeting (UM web service)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (UM web service)](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType (UM web service)](greetingtype-um-web-service.md)
  
[dialString (UM web service)](dialstring-um-web-service.md)

