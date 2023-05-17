---
title: "SubscriptionStatus"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: "The SubscriptionStatus element describes the status of a push subscription."
---

# SubscriptionStatus

The **SubscriptionStatus** element describes the status of a push subscription. 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |Contains the response of the client application' to a push notification.  <br/> |
   
## Text value

A text value is required. The following are the possible text values for this element:
  
- OK
    
- Unsubscribe
    
## Remarks

This element describes the status of the subscription. The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification. If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription. If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

