---
title: "DeliveryStatus"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: "The DeliveryStatus element specifies the status for a message."
---

# DeliveryStatus

The **DeliveryStatus** element specifies the status for a message. 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contains information for a single event for a recipient.  <br/> |
   
## Text value

The following table lists the possible text values for the **DeliveryStatus** element. 
  
**DeliveryStatus element values**

|**Value**|**Description**|
|:-----|:-----|
|Unsuccessful  <br/> |Specifies that a message was not delivered.  <br/> |
|Pending  <br/> |Specifies that the message is waiting for approval from a moderator.  <br/> |
|Delivered  <br/> |Specifies that the message was delivered to all of the specified recipients.  <br/> |
|Transferred  <br/> |Specifies that the message was transferred to a server outside the search scope.  <br/> |
|Read  <br/> |Specifies that the message was delivered and read by the recipients.  <br/> |
   
## Remarks

The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

