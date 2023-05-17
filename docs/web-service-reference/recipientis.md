---
title: "RecipientIs"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RecipientIs
api_type:
- schema
ms.assetid: 5d2fd7ce-6137-4b3c-a716-c0218dcc8a09
description: "The RecipientIs element specifies that any recipient of the e-mail message matches any of the specified recipients in the child Value (ProtectionRuleValueType) elements."
---

# RecipientIs

The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements. 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 **ProtectionRuleRecipientIsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) <br/> |Identifies a recipient.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifies the condition that must be satisfied for the action part of the rule to be executed.  <br/> |
|[And (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Indicates that all child elements must match to evaluate to **true**.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

