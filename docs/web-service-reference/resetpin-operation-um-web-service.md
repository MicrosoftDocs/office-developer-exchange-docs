---
title: "ResetPIN operation (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: "The ResetPIN operation changes the PIN (TUI password) to a new random value."
 
 
---

# ResetPIN operation (UM web service)

The ResetPIN operation changes the PIN (TUI password) to a new random value.
  
## Remarks

The ResetPIN operation creates a new PIN based on the PIN policies. If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user. If the operation fails, it will throw an exception that contains information about the failure.
  
## ResetPIN request example

### Description

The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## Successful ResetPIN response example

### Description

The following example of a ResetPIN response shows a response to the ResetPIN request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## See also



[ResetPIN (UM web service)](resetpin-um-web-service.md)
  
[ResetPINResponse (UM web service)](resetpinresponse-um-web-service.md)

