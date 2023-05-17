---
title: "RecipientTrackingEvent"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: "The RecipientTrackingEvent element contains information for a single event for a recipient."
---

# RecipientTrackingEvent

The **RecipientTrackingEvent** element contains information for a single event for a recipient. 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 **RecipientTrackingEventType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Date (MessageTracking)](date-messagetracking.md) <br/> |This element is required.  <br/> |
|[Recipient](recipient.md) <br/> |This element is required.  <br/> |
|[DeliveryStatus](deliverystatus.md) <br/> |This element is required.  <br/> |
|[EventDescription](eventdescription.md) <br/> |This element is required.  <br/> |
|[EventData](eventdata.md) <br/> |This element is optional.  <br/> |
|[Server (MessageTracking)](server-messagetracking.md) <br/> |This element is required.  <br/> |
|[InternalId](internalid.md) <br/> |This element is required.  <br/> |
|[BccRecipient](bccrecipient.md) <br/> |This element is optional.  <br/> |
|[HiddenRecipient](hiddenrecipient.md) <br/> |This element is optional.  <br/> |
|[UniquePathId](uniquepathid.md) <br/> |This element is optional.  <br/> |
|[RootAddress](rootaddress.md) <br/> |This element is optional.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Contains a list of one or more tracking events for a recipient.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

