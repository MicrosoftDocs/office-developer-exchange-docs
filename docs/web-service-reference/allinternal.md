---
title: "AllInternal"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AllInternal
api_type:
- schema
ms.assetid: b7e5072f-5d9f-4ee0-b58b-4d75d878ea1c
description: "The AllInternal element evaluates to true if all recipients of an e-mail message are internal to the sender's organization."
---

# AllInternal

The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization. 
  
```xml
<AllInternal/>
```

 **ProtectionRuleAllInternalType**
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

The **AllInternal** element must be empty. 
  
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

