---
title: "State (TeamMailboxLifecycleStateType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: "The State element contains the lifecycle state that is set on a site mailbox."
---

# State (TeamMailboxLifecycleStateType)

The **State** element contains the lifecycle state that is set on a site mailbox. 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetTeamMailbox](setteammailbox.md)
  
## Text value

The text value of the **State** element is the lifecycle state that is set on a site mailbox. A text value of **Active** indicates that a site mailbox is in active use. A text value of **Closed** indicates that a site mailbox has been closed and is not in active use. A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment. The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values. A text value of **PendingDelete** indicates that a site mailbox is pending deletion. A site mailbox has to be closed before it can be set as **PendingDelete**.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   