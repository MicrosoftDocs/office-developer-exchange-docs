---
title: "Mailbox"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: "The Mailbox element identifies a mail-enabled Active Directory object."
---

# Mailbox

The **Mailbox** element identifies a mail-enabled Active Directory object. 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

**EmailAddressType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Defines the name of the mailbox user. This element is optional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Defines the mailbox type of a mailbox user. This element is optional.  <br/> |
|[ItemId](itemid.md) <br/> |Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |Defines a request to expand a distribution list. <br/> <br/> The following is the XPath expression to this element: ` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |Contains an array of recipients of an item.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Represents a collection of recipients that will receive a copy of the message.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifies an array of e-mail addresses to which replies should be sent.  <br/> |
|[Sender](sender.md) <br/> |Identifies the sender of an item.  <br/> |
|[From](from.md) <br/> |Represents the addressee from whom the message was sent.  <br/> |
|[Organizer](organizer.md) <br/> |Represents the organizer of a meeting.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | Identifies default Microsoft Exchange Server 2007 folders.  <br/><br/>  The following are the XPath expressions to this element: <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[Resolution](resolution.md) <br/> |Contains a single resolved entity.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contains an array of mailboxes that are contained in a distribution list.  <br/> |
|[Attendee](attendee.md) <br/> |Represents attendees and resources for a calendar item.  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |Defines a request to add managed folders to a mailbox.  <br/> |
|[AddDelegate](adddelegate.md) <br/> |Defines a request to add delegates to a mailbox.  <br/> |
|[GetDelegate](getdelegate.md) <br/> |Defines a request to get information about delegates to a mailbox.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Defines a request to remove delegates from a mailbox.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Defines a request to update delegates in a mailbox.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Describes the delegate in a delegate access scenario.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Describes the principal in a delegate access scenario.  <br/> |
|[Member](member-ex15websvcsotherref.md) <br/> |Represents a member of a distribution list.  <br/> |
   
## Text value

None.
  
## Remarks

The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) and [ItemId](itemid.md) elements identify a mailbox or distribution list. 

The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element identifies a mailbox or distribution list by SMTP address. 

The [ItemId](itemid.md) element identifies a mailbox by an item identifier, which is associated with a particular mailbox. 

The [ItemId](itemid.md) element cannot be used for sending a message to a distribution list or a contact in a public contacts folder. An error will be thrown if this is used in a CreateItem, UpdateItem, or SendItem operation when an attempt is made to send a message to a distribution list or contact in a contacts public folder. Use the ExpandDL operation to get the SMTP address and then send the message by using the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element instead of the [ItemId](itemid.md) element. 
  
Another element, [Mailbox (Availability)](mailbox-availability.md), provides information for availability operations. 
  
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

