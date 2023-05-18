---
title: "GetStreamingEvents"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: "The GetStreamingEvents element represents the operation that is used by clients to request streaming notifications from the server."
---

# GetStreamingEvents

The **GetStreamingEvents** element represents the operation that is used by clients to request streaming notifications from the server. 
  
[GetStreamingEvents](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionIds>
     <SubscriptionId/>
   </SubscriptionIds>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 **GetStreamingEventsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SubscriptionIds](subscriptionids.md) <br/> |Contains an array of subscription identifiers that identify the subscriptions to get streaming events for.  <br/> |
|[ConnectionTimeout](connectiontimeout.md) <br/> |Represents the number of minutes to keep a connection open.  <br/> |
   
### Parent elements

None.
  
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
  
[GetStreamingEvents operation](getstreamingevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

