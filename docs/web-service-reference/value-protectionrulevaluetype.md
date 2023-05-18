---
title: "Value (ProtectionRuleValueType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: b039bd6e-2198-47cf-9c78-a5e8b9d51c98
description: "The Value element identifies a single recipient or sender department."
---

# Value (ProtectionRuleValueType)

The **Value** element identifies a single recipient or sender department. 
  
```XML
<Value/>
```

**ProtectionRuleValueType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientIs](recipientis.md) <br/> |Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.  <br/> |
   
## Text value

This element must contain a nonempty string value.
  
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