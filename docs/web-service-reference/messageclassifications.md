---
title: "MessageClassifications"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MessageClassifications
api_type:
- schema
ms.assetid: 041b3d48-8f43-47f3-869f-72b66bef372a
description: "The MessageClassifications element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply."
---

# MessageClassifications

The **MessageClassifications** element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply. 
  
```XML
<MessageClassifications>
    <String/>
</MessageClassifications>
```

 **ArrayOfStringsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[String](string.md) <br/> |Represents a message classification.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.  <br/> |
   
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

