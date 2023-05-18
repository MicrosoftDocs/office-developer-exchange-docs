---
title: "PrimarySmtpAddress (string)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 706c6387-c648-4ccc-85e6-12a07b66da2f
description: "The PrimarySmtpAddress element specifies the primary Simple Mail Transfer Protocol (SMTP) address of the mailbox."
---

# PrimarySmtpAddress (string)

The **PrimarySmtpAddress** element specifies the primary Simple Mail Transfer Protocol (SMTP) address of the mailbox. 
  
```XML
<PrimarySmtpAddress></PrimarySmtpAddress>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[UserId (string)](userid-string.md) | [Mailbox (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [SearchableMailbox](searchablemailbox.md)
  
## Text value

The text value of the **PrimarySmtpAddress** element is the primary SMTP address of the mailbox. 
  
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
   

