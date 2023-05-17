---
title: "Entry (EmailAddress)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: "The Entry element represents a single e-mail address for a contact."
---

# Entry (EmailAddress)

The **Entry** element represents a single e-mail address for a contact. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Key** <br/> | Identifies the e-mail address.<br/><br/>The following are the possible values for this attribute:<br/><br/>- EmailAddress1  <br/>- EmailAddress2  <br/>- EmailAddress3 <br/><br/>  This attribute is required.  <br/> |
|**Name** <br/> |Defines the name of the mailbox user. This attribute is optional.  <br/> |
|**RoutingType** <br/> |Defines the routing that is used for the mailbox. The default is SMTP. This attribute is optional.  <br/> |
|**MailboxType** <br/> |Defines the mailbox type of a mailbox user. This attribute is optional.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Represents a collection of e-mail addresses for a contact.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

