---
title: "PullSubscriptionRequest"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: "The PullSubscriptionRequest element represents a subscription to a pull-based event notification subscription."
---

# PullSubscriptionRequest

The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription. 
  
[Subscribe](subscribe.md)
  
[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 **PullSubscriptionRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Indicates whether to subscribe to all available folders. This attribute is optional.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Contains a collection of event notifications that are used to create a subscription.  <br/> |
|[Watermark](watermark.md) <br/> |Represents an event bookmark in the mailbox events table. This is used to create a subscription that starts at an event that is represented by the watermark. If the watermark from a Subscribe request is not found, an error response will be returned to the client. This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.  <br/> |
|[Timeout](timeout.md) <br/> |Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |Contains the properties that are used to create subscriptions.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

