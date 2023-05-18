---
title: "Condition"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: "The Condition element identifies the condition that must be satisfied for the action part of the rule to be executed."
---

# Condition

The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed. 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

**ProtectionRuleConditionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.  <br/> |
|[And (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Specifies that all child elements must match to evaluate to **true**. Specifies that there must be more than one protection rule child condition.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.  <br/> |
|[True](true.md) <br/> |Specifies a condition that always matches.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contains a single protection rule.  <br/> |
   
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

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

