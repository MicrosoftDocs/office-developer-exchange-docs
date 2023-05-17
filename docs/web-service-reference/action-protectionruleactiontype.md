---
title: "Action (ProtectionRuleActionType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: "The Action element identifies what action must be executed if the condition part of the rule matches."
---

# Action (ProtectionRuleActionType)

The **Action** element identifies what action must be executed if the condition part of the rule matches. 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 **ProtectionRuleActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Name** <br/> |Identifies the name of the action.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Argument](argument.md) <br/> |Specifies arguments to the action. This element will not occur if the specified action does not require arguments to be specified. This element can occur one or more times if an action requires one or more arguments. The **RightsProtectMessage** action will contain a single argument.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contains a single protection rule.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

