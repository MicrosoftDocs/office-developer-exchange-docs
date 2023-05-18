---
title: "Watermark"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: "The Watermark element represents an event bookmark in the mailbox event queue."
---

# Watermark

The **Watermark** element represents an event bookmark in the mailbox event queue. 
  
```xml
<Watermark/>
```

 **WatermarkType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Represents a subscription to a pull-based event notification subscription.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Represents a subscription to a push-based event notification subscription.  <br/> |
|[GetEvents](getevents.md) <br/> |Represents the operation used by pull clients to request notifications from the server.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Represents an event where an item or folder is copied.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Represents an event where an item or folder is created.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Represents an event where an item or folder is deleted.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Represents an event where an item or folder is modified.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event where an item or folder is moved from one parent folder to another parent folder.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Represents an event triggered by a new mail item in a mailbox.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Represents a notification that no new activity has occurred in the mailbox.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contains the status and result of a Subscribe request.  <br/> |
   
## Text value

A text value may be required or optional depending on how this element is used.
  
## Remarks

If a Subscribe request contains a watermark, the subscription is created from the watermark forward. If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application. This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table. This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database. 
  
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
