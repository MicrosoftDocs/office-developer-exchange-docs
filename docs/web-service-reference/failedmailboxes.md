---
title: "FailedMailboxes"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: "The FailedMailboxes element specifies an array of mailboxes that failed on search."
---

# FailedMailboxes

The **FailedMailboxes** element specifies an array of mailboxes that failed on search. 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 **ArrayOfFailedSearchMailboxesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FailedMailbox](failedmailbox.md) <br/> |Specifies the error message for a mailbox that failed on search.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchMailboxesResult](searchmailboxesresult.md) <br/> |Contains the result of the **SearchMailboxes** request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

