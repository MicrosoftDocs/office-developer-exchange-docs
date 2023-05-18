---
title: "ValidationErrors"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: "The ValidationErrors element represents an array of rule validation errors on each rule field that has an error."
---

# ValidationErrors

The **ValidationErrors** element represents an array of rule validation errors on each rule field that has an error. 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 **ArrayOfRuleValidationErrorsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Error](error.md) <br/> |Represents a single validation error on a particular rule property value, predicate property value, or action property value  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Represents a rule operation error.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

