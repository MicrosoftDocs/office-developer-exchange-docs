---
title: "IsArchive"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: "The IsArchive element specifies a Boolean value that indicates whether the mailbox is an archive mailbox."
---

# IsArchive

The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox. 
  
```XML
<IsArchive>true | false</IsArchive>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)
  
## Text value

A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox. A value of **false** indicates that the target mailbox is not an archive mailbox. 
  
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
