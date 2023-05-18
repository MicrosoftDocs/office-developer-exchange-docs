---
title: "StreamingSubscriptionRequest"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: "The StreamingSubscriptionRequest element represents a subscription to a streaming event notification subscription."
---

# StreamingSubscriptionRequest

The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription. 
  
[Subscribe](subscribe.md)
  
[StreamingSubscriptionRequest](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 **StreamingSubscriptionRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Indicates whether the server will subscribe to all folders in the user's mailbox. A value of **true** indicates that the server will subscribe.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Contains a collection of event notifications that are used to create a subscription.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |Contains the properties that are used to create subscriptions.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[GetStreamingEvents operation](getstreamingevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)

