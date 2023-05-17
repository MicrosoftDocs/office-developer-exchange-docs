---
title: "RedirectToRecipients"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RedirectToRecipients
api_type:
- schema
ms.assetid: 00ef4a84-76d2-4669-b597-f52abbbc34f5
description: "The RedirectToRecipients element indicates the e-mail addresses to which messages are to be redirected."
---

# RedirectToRecipients

The **RedirectToRecipients** element indicates the e-mail addresses to which messages are to be redirected. 
  
```XML
<RedirectToRecipients>
   <Address/>
</RedirectToRecipients>
```

 **ArrayOfEmailAddressesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Address (EmailAddressType)](address-emailaddresstype.md) <br/> |Represents a fully resolved e-mail address.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Actions](actions.md) <br/> |Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

