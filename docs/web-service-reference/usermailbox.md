---
title: "UserMailbox"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: "The UserMailbox element identifies a user mailbox."
---

# UserMailbox

The **UserMailbox** element identifies a user mailbox. 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 **UserMailboxType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The text value of the **Id** attribute is the identifier of the mailbox.  <br/> |
|IsArchive  <br/> |The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox. A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox. A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.  <br/> |
   
### Child elements

None.
  
### Parent elements

[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |true  <br/> |
   

