---
title: "ApprovalDecisionMaker"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 12e055c3-e7a4-4dbc-8385-bbf69571a0ce
description: "The ApprovalDecisionMaker element specifies the display name of the person who made the approval decision."
---

# ApprovalDecisionMaker

The **ApprovalDecisionMaker** element specifies the display name of the person who made the approval decision. 
  
```XML
<ApprovalDecisionMaker />
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ApprovalRequestData](approvalrequestdata.md)
  
## Text value

The text value of the **ApprovalDecisionMaker** element is a display name. 
  
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

