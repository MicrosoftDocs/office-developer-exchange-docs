---
title: "Error"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: "The Error element represents a single validation error on a particular rule property value, predicate property value, or action property value."
---

# Error

The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value. 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 **RuleValidationErrorType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldUri (Rule)](fielduri-rule.md) <br/> |Specifies the URI to the rule field that caused the validation error.  <br/> |
|[ErrorCode](errorcode.md) <br/> |Represents a rule validation error code that describes what failed validation for each rule predicate or action.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Represents the reason for the validation error.  <br/> |
|[FieldValue](fieldvalue.md) <br/> |Represents the value of the field that caused the validation error.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |Represents an array of rule validation errors on each rule field that has an error.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

