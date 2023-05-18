---
title: "Properties (ArrayOfTrackingPropertiesType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: "The Properties element contains a list of one or more tracking properties."
---

# Properties (ArrayOfTrackingPropertiesType)

The **Properties** element contains a list of one or more tracking properties. 
  
- [FindMessageTrackingReport](findmessagetrackingreport.md)
  
- [Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

**ArrayOfTrackingPropertiesType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Represents a name and value pair of strings that is used to create properties for message tracking reports.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Specifies criteria for the types of messages to find.  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contains information for a single event for a recipient.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md)
- [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

