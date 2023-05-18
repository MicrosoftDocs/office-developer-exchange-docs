---
title: "InboxRules"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InboxRules
api_type:
- schema
ms.assetid: 7bb9896c-bd12-49ae-842a-a10b5f9a2ef6
description: "The InboxRules element represents an array of rules in the user's mailbox."
---

# InboxRules

The **InboxRules** element represents an array of rules in the user's mailbox. 
  
[GetInboxRulesResponse](getinboxrulesresponse.md)
  
[InboxRules](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 **ArrayOfRulesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Contains a single rule and represents a rule in the user's mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.  <br/> |
   
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
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetInboxRules](getinboxrules.md)
  
[GetInboxRules operation](getinboxrules-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

