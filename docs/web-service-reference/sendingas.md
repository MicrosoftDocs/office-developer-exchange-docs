---
title: "SendingAs"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SendingAs
api_type:
- schema
ms.assetid: b43ce19f-9ab0-4946-acb2-c5aafead9d35
description: "The SendingAs element represents an e-mail address that a user is trying to send as."
---

# SendingAs

The **SendingAs** element represents an e-mail address that a user is trying to send as. 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 **EmailAddressType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Represents the name of the mailbox user. This element is optional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Defines the address type for the mailbox. The default is SMTP. This element is optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Represents the type of mailbox that is represented by an e-mail user. This element is optional.  <br/> |
|[ItemId](itemid.md) <br/> |Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contains the recipients and types of mail tips to retrieve.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
