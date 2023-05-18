---
title: "IsEncrypted"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsEncrypted
api_type:
- schema
ms.assetid: 68a30e92-c2b1-4af5-bb16-ba38afb80c43
description: "The IsEncrypted element indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply."
---

# IsEncrypted

The **IsEncrypted** element indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply. 
  
```XML
<IsEncrypted>true | false</IsEncrypted>
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
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents all the available rule exception conditions for an Inbox rule.  <br/> |
   
## Text value

A text value of **true** indicates that the message must be S/MIME encrypted in order for the condition or exception to apply. A value of **false** indicates that the message does not have to be S/MIME in order for the condition or exception to apply. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

