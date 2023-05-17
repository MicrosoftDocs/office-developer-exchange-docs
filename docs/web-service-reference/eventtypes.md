---
title: "EventTypes"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EventTypes
api_type:
- schema
ms.assetid: 29ded9e5-f191-4aa3-bc3e-500de2fc8818
description: "The EventTypes element contains a collection of event notification types that are used to create a subscription."
---

# EventTypes

The **EventTypes** element contains a collection of event notification types that are used to create a subscription. 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 **NonEmptyArrayOfNotificationEventTypesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[EventType](eventtype.md) <br/> |Represents a requested event notification type that is used to create a subscription.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Represents a subscription to a pull-based event notification subscription.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Represents a subscription to a push-based event notification subscription.  <br/> |
|[StreamingSubscriptionRequest](streamingsubscriptionrequest.md) <br/> |Represents a subscription to a streaming event notification subscription.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[GetStreamingEvents operation](getstreamingevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)

