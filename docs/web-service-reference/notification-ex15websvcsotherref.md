---
title: "Notification"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: "The Notification element contains information about the subscription and the events that have occurred since the last notification."
---

# Notification

The **Notification** element contains information about the subscription and the events that have occurred since the last notification. 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

**NotificationType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |Represents the identifier for a subscription.  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |Represents the watermark of the latest event that was successfully communicated to the client for the subscription.  <br/> |
|[MoreEvents](moreevents.md) <br/> |Indicates whether there are more events in the queue to be delivered to the client.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Represents an event in which an item or folder is copied.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Represents an event in which an item or folder is created.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Represents an event in which an item or folder is deleted.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Represents an event in which an item or folder is modified.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event in which an item or folder is moved from one parent folder to another parent folder.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Represents an event that is triggered by a new mail item in a mailbox.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Represents a notification that no new activity has occurred in the mailbox.  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |Represents an event in which an item's free/busy time has changed.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contains the status and result of a single GetEvents request.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contains the status and result of a single SendNotification request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Subscribe operation](subscribe-operation.md) 
- [GetEvents operation](getevents-operation.md) 
- [GetStreamingEvents operation](getstreamingevents-operation.md) 
- [Unsubscribe operation](unsubscribe-operation.md)

