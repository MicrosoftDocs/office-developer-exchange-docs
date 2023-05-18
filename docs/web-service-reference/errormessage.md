---
title: "ErrorMessage"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: "The ErrorMessage element represents the reason for the validation error."
---

# ErrorMessage

The **ErrorMessage** element represents the reason for the validation error. 
  
```XML
<ErrorMessage/>
```

 **String**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Error](error.md) <br/> |Represents a single validation error on a particular rule property value, predicate property value, or action property value.  <br/> |
   
## Text value

The error message associated with the rule validation error.
  
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

