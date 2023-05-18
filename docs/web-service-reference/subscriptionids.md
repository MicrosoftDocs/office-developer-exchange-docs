---
title: "SubscriptionIds"
 
 
manager: sethgros
ms.date: 10/18/2021
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SubscriptionIds
api_type:
- schema
ms.assetid: 
description: "The SubscriptionIds element contains an array of subscription identifiers that identify the subscriptions to get streaming events for."
---

# SubscriptionIds

The **SubscriptionIds** element contains an array of subscription identifiers that identify the subscriptions to get streaming events for. 

```XML
<SubscriptionIds>
   <SubscriptionId/>
</SubscriptionIds>
```

 **NonEmptyArrayOfSubscriptionIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) <br/> |Represents the identifier for a subscription that is queried for events.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetStreamingEvents](getstreamingevents.md) <br/> |Represents the operation that is used by clients to request streaming notifications from the server.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |

## See also

[GetStreamingEvents operation](getstreamingevents-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
