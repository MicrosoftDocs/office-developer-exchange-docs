---
title: "CreateRuleOperation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateRuleOperation
api_type:
- schema
ms.assetid: e9f70726-db08-4089-839e-a41007d0a473
description: "The CreateRuleOperation element represents an operation to create a new Inbox rule."
---

# CreateRuleOperation

The **CreateRuleOperation** element represents an operation to create a new Inbox rule. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[Operations](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 **CreateRuleOperationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Represents a rule to be created in a user's mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Operations](operations.md) <br/> |Contains the operations that can be performed on an Inbox.  <br/> |
   
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
  
[SetRuleOperation](setruleoperation.md)
  
[DeleteRuleOperation](deleteruleoperation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

