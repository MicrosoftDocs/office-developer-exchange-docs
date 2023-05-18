---
title: "FailedMailbox"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: "The FailedMailbox element specifies the error message for a mailbox that failed on search."
---

# FailedMailbox

The **FailedMailbox** element specifies the error message for a mailbox that failed on search. 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 **FailedSearchMailboxType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox (string)](mailbox-string.md) <br/> |Contains an identifier for the mailbox.  <br/> |
|[ErrorCode (int)](errorcode-int.md) <br/> |Specifies the error code of the mailbox that failed the search.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Represents the reason for the validation error.  <br/> |
|[IsArchive](isarchive.md) <br/> |Specifies a Boolean value that indicates whether the mailbox is an archive.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FailedMailboxes](failedmailboxes.md) <br/> |Specifies an array of failed mailboxes.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

