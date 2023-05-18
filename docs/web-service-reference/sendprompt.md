---
title: "SendPrompt"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: "The SendPrompt element specifies the type of action allowed for a voting option."
---

# SendPrompt

The **SendPrompt** element specifies the type of action allowed for a voting option. 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[VotingOptionData](votingoptiondata.md)
  
## Text value

The text value of the **SendPrompt** element is a voting option action. The following table lists the possible values for this element. 
  
****

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |No action.  <br/> |
|Send  <br/> |The response is sent immediately.  <br/> |
|VotingOption  <br/> |The approver can enter comments while approving or rejecting.  <br/> |
   
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



[VotingOptionData](votingoptiondata.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

