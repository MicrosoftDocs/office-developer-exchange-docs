---
title: "IncludeNonIndexableItems"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: "The IncludeNonIndexableItems element contains a Boolean value to indicate whether to include items that cannot be indexed."
---

# IncludeNonIndexableItems

The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed. 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## Text value

A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds. A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

