---
title: "PushSubscriptionRequest"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: "The PushSubscriptionRequest element represents a subscription to a push-based event notification subscription."
---

# PushSubscriptionRequest

The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription. 
  
[Subscribe](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 **PushSubscriptionRequestType**
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
|[Watermark](watermark.md) <br/> |Represents an event bookmark in the mailbox events table. This is used to create a subscription starting at an event represented by the watermark. If the watermark from a Subscribe request is not found, an error response will be returned to the client. This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.  <br/> |
|[Url ](url-ex15websvcsotherref.md) <br/> |Represents the location of the client Web service for push notifications.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |Contains the properties used to create subscriptions.  <br/> |
   
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

[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)