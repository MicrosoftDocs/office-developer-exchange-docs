---
title: "MessageTrackingReportId"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- MessageTrackingReportId
api_type:
- schema
ms.assetid: 9c604ca3-10fe-4760-b7fd-8b52f1a0c712
description: "The MessageTrackingReportId element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message."
---

# MessageTrackingReportId

The **MessageTrackingReportId** element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message. 
  
```XML
<MessageTrackingReportId/>
```

 **NonEmptyStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.  <br/> |
   
## Text value

A text value that represents a string is required if this element is used.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

