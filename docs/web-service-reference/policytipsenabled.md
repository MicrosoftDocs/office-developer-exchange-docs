---
title: "PolicyTipsEnabled"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 16409652-21e4-4bd3-9373-67e1882236b4
description: "The PolicyTipsEnabled element indicates whether policy tips are enabled."
---

# PolicyTipsEnabled

The **PolicyTipsEnabled** element indicates whether policy tips are enabled. 
  
```XML
<PolicyTipsEnabled> true | false </PolicyTipsEnabled>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md)
  
## Text value

A text value of **true** for the **PolicyTipsEnabled** element indicates that policy tips are enabled for a mailbox. A value of **false** indicates that policy tips are not enabled for a mailbox. 
  
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
   

