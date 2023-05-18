---
title: "PreviousWatermark"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: "The PreviousWatermark element represents the watermark of the latest event that was successfully communicated to the client for the subscription."
---

# PreviousWatermark

The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription. 
  
```xml
<PreviousWatermark/>
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
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Text value

A text value is required. The text value represents the latest watermark. The text value cannot be an empty string.
  
## Remarks

The **PreviousWatermark** property is useful to the client in determining the last successful notification. For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received. This enables the client to ensure the continuity of events. 
  
For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark. If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark. For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark. 
  
In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)

