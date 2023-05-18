---
title: "MailTipsRequested"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: "The MailTipsRequested element contains the types of mail tips requested from the service."
---

# MailTipsRequested

The **MailTipsRequested** element contains the types of mail tips requested from the service. 
  
```XML
<MailTipsRequested/>
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
|[GetMailTips](getmailtips.md) <br/> |Contains the recipients and types of mail tips to retrieve.  <br/> |
   
## Text value

The following table lists the possible values for the **MailTipsRequested** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|All  <br/> |Represents all available mail tips.  <br/> |
|OutOfOfficeMessage  <br/> |Represents the Out of Office (OOF) message.  <br/> |
|MailboxFullStatus  <br/> |Represents the status for a mailbox that is full.  <br/> |
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

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

