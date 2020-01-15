---
title: "RuleOperationError"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleOperationError
api_type:
- schema
ms.assetid: b447e610-d37c-40d3-9158-aa108a9f248e
description: "The RuleOperationError element represents a rule operation error."
---

# RuleOperationError

The **RuleOperationError** element represents a rule operation error. 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 **RuleOperationErrorType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[OperationIndex](operationindex.md) <br/> |Indicates the index of the operation in the request that caused the rule operation error.  <br/> |
|[ValidationErrors](validationerrors.md) <br/> |Represents an array of rule validation errors on each rule field that has an error.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RuleOperationErrors](ruleoperationerrors.md) <br/> |Represents an array of rule validation errors on each rule field that has an error.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

