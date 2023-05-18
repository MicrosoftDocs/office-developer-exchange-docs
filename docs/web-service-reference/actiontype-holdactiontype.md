---
title: "ActionType (HoldActionType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: "The ActionType element indicates the type of action for the hold."
---

# ActionType (HoldActionType)

The **ActionType** element indicates the type of action for the hold. 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 **HoldActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## Text value

The text value of the **ActionType** element is the type of hold set on a mailbox. A text value of **Create** indicates that a mailbox hold will be created. A text value of **Update** indicates that a mailbox hold will be updated. A text value of **Remove** indicates that a mailbox hold will be removed. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

