---
title: "Address (EmailAddressType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: "The Address element represents a fully resolved e-mail address."
---

# Address (EmailAddressType)

The **Address** element represents a fully resolved e-mail address. 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
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
|[ItemId](itemid.md) <br/> |Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OriginalRecipients](originalrecipients.md) <br/> |Contains a collection of e-mail addresses that represent the original recipients of a tracked message.  <br/> |
|[RoomLists](roomlists.md) <br/> |Contains a list of meeting rooms in an organization.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) 
- [GetRoomLists operation](getroomlists-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

