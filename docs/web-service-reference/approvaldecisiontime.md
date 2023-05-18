---
title: "ApprovalDecisionTime"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e70f1a3d-03cf-4252-804f-3eef0ce4a1a9
description: "The ApprovalDecisionTime element specifies the time at which the approval decision was made."
---

# ApprovalDecisionTime

The **ApprovalDecisionTime** element specifies the time at which the approval decision was made. 
  
```XML
<ApprovalDecisionTime />
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ApprovalRequestData](approvalrequestdata.md)
  
## Text value

The text value of the **ApprovalDecisionTime** element represents the time and date at which the approval decision was made. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [ApprovalRequestData](approvalrequestdata.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

