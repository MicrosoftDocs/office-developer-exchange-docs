---
title: "VotingInformation"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: "The VotingInformation element specifies voting information on a voting message and approval request message whereApproveandRejectare the voting options."
---

# VotingInformation

The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options. 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 **VotingInformationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)
  
### Parent elements

[Message](message-ex15websvcsotherref.md)
  
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



[Message](message-ex15websvcsotherref.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

