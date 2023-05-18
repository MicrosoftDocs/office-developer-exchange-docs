---
title: "SetRuleOperation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SetRuleOperation
api_type:
- schema
ms.assetid: 2106a85b-58fe-49be-b71d-4ca6aa66e060
description: "The SetRuleOperation element represents an operation to update an existing rule."
---

# SetRuleOperation

The **SetRuleOperation** element represents an operation to update an existing rule. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[Operations](operations.md)
  
```XML
<SetRuleOperation>
    <Rule/>
</SetRuleOperation>
```

 **SetRuleOperationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Represents a rule in a user's mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Operations](operations.md) <br/> |Contains an array of rule operations that can be performed on an Inbox.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[UpdateInboxRules](updateinboxrules.md)
  
[DeleteRuleOperation](deleteruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

