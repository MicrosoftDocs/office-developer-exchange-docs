---
title: "Status (HoldStatusType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: "The Status element specifies the hold status for a mailbox."
---

# Status (HoldStatusType)

The **Status** element specifies the hold status for a mailbox. 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[MailboxHoldStatus](mailboxholdstatus.md)
  
## Text value

The text value of the **Status** element is the hold status of a mailbox. The **Status** element can have the values in the following list. 
  
> NotOnHold - The mailbox is not on hold.
    
> Pending - The mailbox is pending either being placed or released on hold. 
    
> OnHold - The hold was successfully applied to the mailbox. 
    
> PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.
    
> Failed - The hold failed to apply to the mailbox.
    
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

