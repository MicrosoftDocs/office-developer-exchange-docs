---
title: "Senders"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 69d88bb1-397c-4fb8-bd2b-21cccc5bb35d
description: "The Senders element specifies an array of Simple Mail Transfer Protocol (SMTP) addresses."
---

# Senders

The **Senders** element specifies an array of Simple Mail Transfer Protocol (SMTP) addresses. 
  
```XML
<Senders>
   <SmtpAddress/>
</Senders>
```

 **ArrayOfSmtpAddressType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[SmtpAddress](smtpaddress.md)
  
### Parent elements

[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

