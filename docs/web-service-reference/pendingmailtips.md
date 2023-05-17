---
title: "PendingMailTips"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: "The PendingMailTips element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired."
---

# PendingMailTips

The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired. 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 **MailTipTypes**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTips](mailtips.md) <br/> |Represents values for various types of mail tips.  <br/> |
   
## Text value

The following table lists the possible values for the **PendingMailTips** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|All  <br/> |Represents all available mail tips.  <br/> |
|OutOfOfficeMessage  <br/> |Represents the Out of Office (OOF) message.  <br/> |
|MailboxFullStatus  <br/> |Represents the status for a mailbox being full.  <br/> |
|CustomMailTip  <br/> |Represents a custom mail tip.  <br/> |
|ExternalMemberCount  <br/> |Represents the count of external members.  <br/> |
|TotalMemberCount  <br/> |Represents the count of all members.  <br/> |
|MaxMessageSize  <br/> |Represents the maximum message size a recipient can accept.  <br/> |
|DeliveryRestriction  <br/> |Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.  <br/> |
|ModerationStatus  <br/> |Indicates whether the sender's message will be reviewed by a moderator.  <br/> |
|InvalidRecipient  <br/> |Indicates whether the recipient is invalid.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

