---
title: "And (ProtectionRuleAndType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: "The And element specifies that all child elements must match to evaluate to true."
---

# And (ProtectionRuleAndType)

The **And** element specifies that all child elements must match to evaluate to **true**.
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 **ProtectionRuleAndType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.  <br/> |
|**And** <br/> |Specifies that all child elements must match to evaluate to **true**.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.  <br/> |
|[True](true.md) <br/> |Specifies a condition that always matches.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifies the condition that must be satisfied for the action part of the rule to be executed.  <br/> |
|**And** <br/> |Specifies that all child elements must match to evaluate to **true**.  <br/> |
   
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

