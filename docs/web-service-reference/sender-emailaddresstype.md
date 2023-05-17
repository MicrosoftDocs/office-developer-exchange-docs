---
title: "Sender (EmailAddressType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Sender
api_type:
- schema
ms.assetid: 717eb6d0-d167-4b20-92e2-5d08b96186c4
description: "The Sender element represents the e-mail address for the sender of the message."
---

# Sender (EmailAddressType)

The **Sender** element represents the e-mail address for the sender of the message. 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
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
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Represents the routing protocol for the recipient. The default value is SMTP. This element is optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Represents the type of mailbox that is represented by the e-mail address. This element is optional.  <br/> |
|[ItemId](itemid.md) <br/> |Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Specifies criteria for the types of messages to find.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).  <br/> |
   
## Text value

None.
  
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



[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

