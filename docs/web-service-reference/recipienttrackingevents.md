---
title: "RecipientTrackingEvents"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: "The RecipientTrackingEvents element represents a collection of one or more events for a message."
---

# RecipientTrackingEvents

The **RecipientTrackingEvents** element represents a collection of one or more events for a message. 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 **ArrayOfRecipientTrackingEventType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contains details for a specific event in the tracking report.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

