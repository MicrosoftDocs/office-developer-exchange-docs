---
title: "ApprovalDecision"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: "The ApprovalDecision element specifies the decision made on an approval request message."
---

# ApprovalDecision

The **ApprovalDecision** element specifies the decision made on an approval request message. 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ApprovalRequestData](approvalrequestdata.md)
  
## Text value

The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected. 
  
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

