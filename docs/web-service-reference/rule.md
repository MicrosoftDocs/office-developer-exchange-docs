---
title: "Rule"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: "The Rule element contains a single protection rule."
---

# Rule

The **Rule** element contains a single protection rule. 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 **ProtectionRuleType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Name** <br/> |Identifies the name of the rule. A required attribute of type string with a minimum length of 1.  <br/> |
|**UserOverridable** <br/> |Specifies whether the rule is mandatory. If the rule is mandatory, this attribute value must be **false**. A required attribute of type Boolean.  <br/> |
|**Priority** <br/> |Specifies the rule priority. A required attribute of type int with a minimum value of 1.  <br/> |
   
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifies the condition that must be satisfied for the action part of the rule to be executed.  <br/> |
|[Action (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |Identifies what action must be executed if the condition part of the rule matches.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rules ](rules-ex15websvcsotherref.md) <br/> |Contains an array of protection rules.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

