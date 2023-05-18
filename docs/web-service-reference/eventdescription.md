---
title: "EventDescription"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EventDescription
api_type:
- schema
ms.assetid: 7642cb03-71b1-4773-9508-4fbe3a5dcdf4
description: "The EventDescription element"
---

# EventDescription

The **EventDescription** element 
  
```xml
<EventDescription/>
```

 **MessageTrackingEventDescriptionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> ||
   
## Text value

The following table lists the possible values for the **EventDescription** element. 
  
**EventDescription element values**

|**Value**|**Description**|
|:-----|:-----|
|Submitted  <br/> ||
|Resolved  <br/> ||
|Expanded  <br/> ||
|Delivered  <br/> ||
|MovedToFolderByInboxRule  <br/> ||
|RulesCc  <br/> ||
|FailedGeneral  <br/> ||
|FailedModeration  <br/> ||
|FailedTransportRules  <br/> ||
|SmtpSend  <br/> ||
|SmtpSendCrossSite  <br/> ||
|SmtpSendCrossForest  <br/> ||
|SmtpReceive  <br/> ||
|Forwarded  <br/> ||
|Pending  <br/> ||
|PendingModeration  <br/> ||
|ApprovedModeration  <br/> ||
|QueueRetry  <br/> ||
|QueueRetryNoRetryTime  <br/> ||
|MessageDefer  <br/> ||
|TransferredToForeignOrg  <br/> ||
|TransferredToPartnerOrg  <br/> ||
|TransferredToLegacyExchangeServer  <br/> ||
|DelayedAfterTransferToPartnerOrg  <br/> ||
|Read  <br/> ||
|NotRead  <br/> ||
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

