---
title: "GetMessageTrackingReport"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: "The GetMessageTrackingReport element contains the request for the GetMessageTrackingReport operation to retrieve the full message tracking report for the specified ID."
---

# GetMessageTrackingReport

The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID. 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 **GetMessageTrackingReportRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Specifies where to perform the search. This element is required.  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |Specifies the type of tracking report to retrieve. This element is required.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Specifies a recipient address to use with the specified tracking report. This element is optional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation. This element is required.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Specifies that the person who is running the task has a privileged role. This element is optional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Specifies timing and performance information that will be used to derive the tracking report. This element is optional.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Specifies a list of one or more tracking properties. This element is optional.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
