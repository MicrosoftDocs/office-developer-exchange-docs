---
title: "StatusEvent"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: "The StatusEvent element represents a notification that no new activity has occurred in the mailbox."
---

# StatusEvent

The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox. 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Represents the last valid watermark for a subscription.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

The **StatusEvent** element is returned in a notification for one of the following reasons: 
  
- A pull client issues a GetEvents request on a subscription that has no activity.
    
- A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached. 
    
The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks. However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events. For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification. A period of inactivity occurs and a **GetEvents** request is sent. The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).
  
The watermark will not remain the same in all cases. Event entries are maintained for 30 days. To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues. The updated watermarks are sent to clients to maintain an active subscription.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
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

