---
title: "IsUMEnabled operation (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: "The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging."
 
 
---

# IsUMEnabled operation (UM web service)

The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging.
  
## IsUMEnabled request example

### Description

The following example of an IsUMEnabled request shows how to form a request to determine whether a mailbox is enabled for Unified Messaging.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## Successful IsUMEnabled response example

### Description

The following example shows a successful response to an IsUMEnabled request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## See also



[IsUMEnabled (UM web service)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (UM web service)](isumenabledresponse-um-web-service.md)


[Unified Messaging web service XML elements for Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

