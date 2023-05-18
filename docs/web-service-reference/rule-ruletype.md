---
title: "Rule (RuleType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Rule
api_type:
- schema
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: "The Rule element contains a single rule and represents a rule in a user's mailbox."
---

# Rule (RuleType)

The **Rule** element contains a single rule and represents a rule in a user's mailbox. 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 **RuleType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RuleId](ruleid.md) <br/> |Specifies the rule identifier.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Contains the display name of a rule.  <br/> |
|[Priority](priority.md) <br/> |Indicates the order in which a rule is to be run.  <br/> |
|[IsEnabled](isenabled.md) <br/> |Indicates whether the rule is enabled.  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |Indicates whether the rule cannot be modified with the managed code APIs.  <br/> |
|[IsInError](isinerror.md) <br/> |Indicates whether the rule is in an error condition.  <br/> |
|[Conditions](conditions.md) <br/> |Identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.  <br/> |
|[Exceptions](exceptions.md) <br/> |Identifies the exceptions that represent all the available rule exception conditions for the inbox rule.  <br/> |
|[Actions](actions.md) <br/> |Represents the actions to be taken on a message when the conditions are fulfilled.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Represents an operation to create a new rule.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Represents an array of rules in the user's mailbox.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Represents an operation to update an existing rule.  <br/> |
   
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
|Can be Empty  <br/> |True  <br/> |
   
## See also



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

