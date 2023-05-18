---
title: "FindMessageTrackingReport"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: "The FindMessageTrackingReport element specifies criteria for the types of messages to find."
---

# FindMessageTrackingReport

The **FindMessageTrackingReport** element specifies criteria for the types of messages to find. 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 **FindMessageTrackingReportRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Represents how extensive the message tracking report should be.  <br/> |
|[Domain (Message Tracking)](domain-message-tracking.md) <br/> |Contains the name of the domain where the message tracking is executed.  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contains contact information for the sender of the e-mail message.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contains contact information for the alleged sender of an e-mail message.  <br/> |
|[Recipient](recipient.md) <br/> |Contains the e-mail address for the recipient of the message.  <br/> |
|[Subject](subject.md) <br/> |Contains the subject of the e-mail message.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Contains the starting date and time for the search.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Contains the ending date and time for the search.  <br/> |
|[MessageId](messageid.md) <br/> |Contains the message identifier for the search.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Contains the name of the mailbox where the cross-premise message was sent.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Represents the level of detail for diagnostic reports.  <br/> |
|[ServerHint](serverhint.md) <br/> |Represents the starting point for tracking a message in a remote site or forest.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contains a list of one or more tracking properties. This element is optional.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindMessageTrackingReport operation](findmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

