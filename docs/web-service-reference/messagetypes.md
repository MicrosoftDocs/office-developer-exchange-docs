---
title: "MessageTypes"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fac1cfe0-8e7b-4196-b3ad-4e86043d9c9b
description: "The MessageTypes element specifies an array of messages to search."
---

# MessageTypes

The **MessageTypes** element specifies an array of messages to search. 
  
```XML
<MessageTypes>
   <SearchItemKind/>
</MessageTypes>
```

 **ArrayOfSearchItemKindsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[SearchItemKind](searchitemkind.md)
  
### Parent elements

[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

