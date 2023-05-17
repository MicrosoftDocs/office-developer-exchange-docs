---
title: "FederatedDeliveryMailbox"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FederatedDeliveryMailbox
api_type:
- schema
ms.assetid: cd56bcc0-d24a-4e8b-87bd-999bf69234b7
description: "The FederatedDeliveryMailbox element represents the mailbox to which a cross-premise message was sent."
---

# FederatedDeliveryMailbox

The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent. 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
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
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Contains criteria for the types of messages to find.  <br/> |
   
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
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

