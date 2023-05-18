---
title: "StatusFrequency"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: "The StatusFrequency element represents the maximum timeout value, in minutes, in which retries are attempted by the server."
---

# StatusFrequency

The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server. 
  
[Subscribe](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Represents a subscription to a push-based event notification subscription.  <br/> |
   
## Text value

A text value that represents an integer is required if this element is used. The possible values for this element are 1 to 1440, inclusive. This element is optional. The default value is 30 minutes.
  
## Remarks

The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client. If the server does not receive a response, it retries sending the notification several times before it stops sending the notification. In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval. Retry times are not exact as they can be delayed due to other loads on the server. The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays). 
  
|**Retry**|**Seconds**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Initial sync  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4  <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6  <br/> |960  <br/> |16:00  <br/> |
|7  <br/> |1920  <br/> |32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent  <br/> |
   
If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)
  
[Watermark](watermark.md)

