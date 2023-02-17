---
title: "EmailAddress (NonEmptyStringType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: "The EmailAddress element defines the primary SMTP address of a mailbox user."
---

# EmailAddress (NonEmptyStringType)

The **EmailAddress** element defines the primary SMTP address of a mailbox user. 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifies who the caller is sending as.  <br/> |
|[Mailbox](mailbox.md) <br/> | Identifies a fully resolved e-mail address.  <br/><br/>The following are some XPath expressions to this element:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>The following are additional parent elements of the Mailbox element:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Sender](sender.md) <br/>- [From](from.md) <br/>- [Organizer](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Resolution](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Attendee](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifies a list of meeting rooms by email address.  <br/> |
   
## Text value

A text value that represents an SMTP address is required.
  
## Remarks

The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses. The **EmailAddress** element is the only required [Mailbox](mailbox.md) element. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

