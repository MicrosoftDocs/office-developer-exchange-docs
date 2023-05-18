---
title: "Operations"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: "The Operations element contains an array of rule operations that can be performed on an Inbox."
---

# Operations

The **Operations** element contains an array of rule operations that can be performed on an Inbox. 
  
[UpdateInboxRules](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 **ArrayOfRuleOperationsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Represents an operation to create a new Inbox rule.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Represents an operation to update an Inbox rule.  <br/> |
|[DeleteRuleOperation](deleteruleoperation.md) <br/> |Represents an operation to delete an Inbox rule.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Defines a request to update the Inbox rules in a mailbox in the server store.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[UpdateInboxRules operation](updateinboxrules-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

