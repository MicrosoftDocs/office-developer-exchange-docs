---
title: "MailboxType"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: "The MailboxType element represents the type of mailbox that is represented by the e-mail address."
---

# MailboxType

The **MailboxType** element represents the type of mailbox that is represented by the e-mail address. 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a fully resolved e-mail address.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifies a list of meeting rooms.  <br/> |
   
## Text value

The following table lists the possible values for the **MailboxType** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|Mailbox  <br/> |Represents a mail-enabled Active Directory object.  <br/> |
|PublicDL  <br/> |Represents a public distribution list.  <br/> |
|PrivateDL  <br/> |Represents a private distribution list in a user's mailbox.  <br/> |
|Contact  <br/> |Represents a contact in a user's mailbox.  <br/> |
|PublicFolder  <br/> |Represents a public folder.  <br/> |
|Unknown  <br/> |Represents an unknown type of mailbox.  <br/> |
|OneOff  <br/> |Represents a one-off member of a personal distribution list.  <br/> |
|GroupMailbox  <br/> |Represents a group mailbox.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

