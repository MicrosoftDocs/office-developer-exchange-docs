---
title: "MessageTrackingSearchResult"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: "The MessageTrackingSearchResult element contains a single message result for a FindMessageTrackingReportResponse element."
---

# MessageTrackingSearchResult

The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element. 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 **FindMessageTrackingSearchResultType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Subject](subject.md) <br/> |Contains the e-mail message subject.  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contains the e-mail message sender's address.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contains contact information for the alleged sender of an e-mail message.  <br/> |
|[Recipients (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Contains a list of e-mail addresses that received this message.  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |Contains the time that the message was submitted.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Contains an internal ID that identifies the message in the transport database.  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |Contains the name of the server in the forest that previously accepted the message.  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |Contains the name of the server in the forest that first accepted the message.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contains a list of one or more tracking properties.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |Contains a list of messages that match the search criteria.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindMessageTrackingReport operation](findmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

