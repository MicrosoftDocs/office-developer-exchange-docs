---
title: "IsReadReceipt"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: "The IsReadReceipt element indicates whether incoming messages must be read receipts in order for the condition or exception to apply."
---

# IsReadReceipt

The **IsReadReceipt** element indicates whether incoming messages must be read receipts in order for the condition or exception to apply. 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents all the available rule exception conditions for the Inbox rule.  <br/> |
   
## Text value

A text value of **true** indicates that the message must be a read receipt in order for the condition or exception to apply. If the message does not have to be a read receipt for the condition or exception to apply, the value is **false**.
  
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
