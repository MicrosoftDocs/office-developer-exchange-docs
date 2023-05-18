---
title: "Diagnostics"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Diagnostics
api_type:
- schema
ms.assetid: fecea440-970a-49da-9796-534ca470cbd6
description: "The Diagnostics element provides timing and performance information that is used for reporting in a DataCenter."
---

# Diagnostics

The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter. 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 **ArrayOfStringsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[String](string.md) <br/> |Contains a string that is used by items, contacts, tasks, and conversations.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).  <br/> |
   
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

- [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md)
- [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

