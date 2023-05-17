---
title: "VotingResponse"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: "The VotingResponse element specifies the submitted vote. This element is only present on responses to voting request messages, not on responses to approvals."
---

# VotingResponse

The **VotingResponse** element specifies the submitted vote. This element is only present on responses to voting request messages, not on responses to approvals. 
  
```XML
<VotingResponse />
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[VotingInformation](votinginformation.md)
  
## Text value

The text value of the **VotingResponse** element is the vote submitted. 
  
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

- [VotingInformation](votinginformation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
