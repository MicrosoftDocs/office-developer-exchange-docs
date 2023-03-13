---
title: "PlayOnPhone operation (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: "The PlayOnPhone operation makes an outbound call and plays a specified message over the telephone that is specified by the DialString element."
 
 
---

# PlayOnPhone operation (UM web service)

The PlayOnPhone operation makes an outbound call and plays a specified message over the telephone that is specified by the **DialString** element. 
  
## PlayOnPhone request example

### Description

The following example of a PlayOnPhone request shows how to form a request to make an outbound call and play a message.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## Successful PlayOnPhone response example

### Description

The following example of a PlayOnPhone response shows a response to the PlayOnPhone request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## See also



[PlayOnPhone (UM web service)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (UM web service)](playonphoneresponse-um-web-service.md)
  
[PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md)

