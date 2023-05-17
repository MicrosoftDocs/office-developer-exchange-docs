---
title: "InPlaceHoldIdentity"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: "The InPlaceHoldIdentity element specifies the identity of a hold that preserves the mailbox items."
---

# InPlaceHoldIdentity

The **InPlaceHoldIdentity** element specifies the identity of a hold that preserves the mailbox items. 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## Text value

The text value of the **InPlaceHoldIdentity** element is the mailbox hold identifier. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SetHoldOnMailboxes operation](setholdonmailboxes-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

