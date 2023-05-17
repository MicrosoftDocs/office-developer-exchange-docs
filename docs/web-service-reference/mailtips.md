---
title: "MailTips"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: "The MailTips element represents values for various types of mail tips."
---

# MailTips

The **MailTips** element represents values for various types of mail tips. 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 **MailTips**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Represents the mailbox of the recipient.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Represents the response message and a duration time for sending the response message.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Indicates whether the mailbox for the recipient is full.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Represents a customized mail tip message.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Represents the count of all members in a group.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Represents the count of external members in a group.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Represents the maximum message size the recipient can accept.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Indicates whether the recipient's mailbox is being moderated.  <br/> |
|[InvalidRecipient (MailTips)](invalidrecipient-mailtips.md) <br/> |Indicates whether the recipient is invalid.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Represents mail tips settings.  <br/> |
   
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

