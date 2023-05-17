---
title: "Timeout (duration)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: "The Timeout element specifies the length of time before a pull subscription is timed out by the server."
---

# Timeout (duration)

The **Timeout** element specifies the length of time before a pull subscription is timed out by the server. 
  
```XML
<Timeout></Timeout>
```

 **SubscriptionTimeoutType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
## Text value

The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server. The minimum value is 1; the maximum value is 1440. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

