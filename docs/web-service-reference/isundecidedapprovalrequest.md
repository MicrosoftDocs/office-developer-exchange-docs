---
title: "IsUndecidedApprovalRequest"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: "The IsUndecidedApprovalRequest element specifies whether an approval request message has been acted on."
---

# IsUndecidedApprovalRequest

The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on. 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ApprovalRequestData](approvalrequestdata.md)
  
## Text value

The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on. A value of **false** indicates that the approval request has been decided. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[ApprovalRequestData](approvalrequestdata.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

