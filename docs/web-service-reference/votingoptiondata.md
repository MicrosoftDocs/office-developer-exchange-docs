---
title: "VotingOptionData"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 387328ae-4dcc-4230-8e4b-01d7894bbce2
description: "The VotingOptionData element specifies information about each voting option."
---

# VotingOptionData

The **VotingOptionData** element specifies information about each voting option. 
  
```XML
<VotingOptionData>
   <DisplayName/>
   <SendPrompt/>
</VotingOptionData>
```

 **VotingOptionDataType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[DisplayName (VotingOptionDataType)](displayname-votingoptiondatatype.md) | [SendPrompt](sendprompt.md)
  
### Parent elements

[UserOptions](useroptions.md)
  
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

- [UserOptions](useroptions.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)