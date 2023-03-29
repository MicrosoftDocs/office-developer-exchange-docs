---
title: "SetMissedCallNotificationEnabled operation (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: "The SetMissedCallNotificationEnabled operation enables or disables missed call notifications."
 
 
---

# SetMissedCallNotificationEnabled operation (UM web service)

The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.
  
## SetMissedCallNotificationEnabled request example

### Description

The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## Successful SetMissedCallNotificationEnabled response example

### Description

The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## See also



[SetMissedCallNotificationEnabled (UM web service)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (UM web service)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status (UM web service - SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)

