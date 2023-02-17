---
title: "Disconnect operation (UM web service)"
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
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: "The Disconnect operation terminates the call that is identified by the specified CallId (UM web service)."
---

# Disconnect operation (UM web service)

The Disconnect operation terminates the call that is identified by the specified [CallId (UM web service)](callid-um-web-service.md).
  
## Disconnect request example

### Description

The following example of a Disconnect request shows how to form a request to disconnect a call.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## Successful Disconnect response example

### Description

The following example of a Disconnect response shows a response to the Disconnect request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## See also

- [Disconnect (UM web service)](disconnect-um-web-service.md) 
- [DisconnectResponse (UM web service)](disconnectresponse-um-web-service.md) 
- [CallId (UM web service)](callid-um-web-service.md)

