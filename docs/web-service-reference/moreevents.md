---
title: "MoreEvents"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: "The MoreEvents element indicates whether there are more events in the queue to be delivered to the client."
---

# MoreEvents

The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.
  
```xml
<MoreEvents/>
```

**Boolean**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md)|Contains information about the subscription and the events that have occurred since the last notification. |

## Text value

The text value represents a Boolean value. A value of **true** indicates that more events are in the queue. A value of **false** indicates that no more events are in the queue. This property is read-only.
  
## Remarks

In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events. Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.
  
In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events. Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace |https://schemas.microsoft.com/exchange/services/2006/types |
|Schema Name |Types schema |
|Validation File |Types.xsd |
|Can be Empty |False |

## See also

[Subscribe operation](subscribe-operation.md)  
[GetEvents operation](getevents-operation.md)  
[Unsubscribe operation](unsubscribe-operation.md)
