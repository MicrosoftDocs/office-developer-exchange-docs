---
title: "True"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 96b4c288-c4d5-4378-8fc1-1a3ae98eedc9
description: "The True element specifies a condition that always matches."
---

# True

The **True** element specifies a condition that always matches. 
  
```xml
<True/>
```

**ProtectionRuleTrueType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifies the condition that must be satisfied for the action part of the rule to be executed.  <br/> |
|[And (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Specifies that all child elements must match to evaluate to **true**.  <br/> |
   
## Text value

This element must be empty.
  
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

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

