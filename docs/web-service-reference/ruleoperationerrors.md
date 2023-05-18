---
title: "RuleOperationErrors"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: "The RuleOperationErrors element represents an array of rule validation errors on each rule field that has an error."
---

# RuleOperationErrors

The **RuleOperationErrors** element represents an array of rule validation errors on each rule field that has an error. 
  
[UpdateInboxRulesResponse](updateinboxrulesresponse.md)
  
[RuleOperationErrors](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 **ArrayOfRuleOperationErrorsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Represents a rule operation error.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Defines a response to an [UpdateInboxRules](updateinboxrules.md) request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |True  <br/> |
   
## See also



[UpdateInboxRules](updateinboxrules.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

