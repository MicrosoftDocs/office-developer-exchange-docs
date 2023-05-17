---
title: "ReportTemplate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: "The ReportTemplate element represents the type of report to get."
---

# ReportTemplate

The **ReportTemplate** element represents the type of report to get. 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 **MessageTrackingReportTemplateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.  <br/> |
   
## Text value

The following table lists the possible values for the **ReportTemplate** element. 
  
**ReportTemplate element values**

|**Value**|**Description**|
|:-----|:-----|
|Summary  <br/> |Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.  <br/> |
|RecipientPath  <br/> |Specifies that for a single recipient, the report will display a full history of the events that occurred.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

