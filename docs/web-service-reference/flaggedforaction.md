---
title: "FlaggedForAction"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FlaggedForAction
api_type:
- schema
ms.assetid: 6a08c48a-7b32-4754-8940-adbda55e8133
description: "The FlaggedForAction element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply."
---

# FlaggedForAction

The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply. 
  
```XML
<FlaggedForAction/>
```

 **FlaggedForActionType**
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
|[Exceptions](exceptions.md) <br/> |Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.  <br/> |
   
## Text value

A text value is required. The following are the possible text values for this element:
  
- Any
    
- Call
    
- DoNotForward
    
- FollowUp
    
- FYI
    
- Forward
    
- NoResponseNecessary
    
- Read
    
- Reply
    
- ReplyToAll
    
- Review
    
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

