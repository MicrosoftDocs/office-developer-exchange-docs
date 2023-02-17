---
title: "AlternateMailbox (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: "The AlternateMailbox element represents an alternate mailbox."
---

# AlternateMailbox (SOAP)

The **AlternateMailbox** element represents an alternate mailbox. 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 **AlternateMailbox**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Type (SOAP)](type-soap.md) <br/> |Represents the alternate mailbox type.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Represents the alternate mailbox display name.  <br/> |
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Represents the alternate mailbox legacy distinguished name.  <br/> |
|[Server (SOAP)](server-soap.md) <br/> |Represents the alternate mailbox server.  <br/> |
|[SmtpAddress (SOAP)](smtpaddress-soap.md) <br/> |Represents the alternate mailbox SMTP address.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AlternateMailboxes (SOAP)](alternatemailboxes-soap.md) <br/> |Represents a collection of alternate mailboxes.  <br/> |
   
## Text value

None.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md)

