---
title: "ErrorSubscriptionIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: "The ErrorSubscriptionIds element contains an array of invalid subscription IDs."
---

# ErrorSubscriptionIds

The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs. 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 **NonEmptyArrayOfSubscriptionIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |Represents the identifier for a subscription.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|Name|Value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Messages schema; Types schema  <br/> |
|Validation File  <br/> |Messages.xsd; Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetStreamingEvents operation](getstreamingevents-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

