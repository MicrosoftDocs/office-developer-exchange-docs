---
title: "UserOptions"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 1acbb8a3-9110-4427-a06c-7e6e627e969f
description: "The UserOptions element specifies the list of voting options on a message."
---

# UserOptions

The **UserOptions** element specifies the list of voting options on a message. 
  
```XML
<UserOptions>
   <VotingOptionData>
</UserOptions>
```

 **ArrayOfVotingOptionDataType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[VotingOptionData](votingoptiondata.md)
  
### Parent elements

[VotingInformation](votinginformation.md)
  
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
