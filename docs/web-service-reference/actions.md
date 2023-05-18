---
title: "Actions"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: "The Actions element represents the set of actions that are available to be taken on a message when the conditions are fulfilled."
---

# Actions

The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled. 
  
[Rule (RuleType)](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 **RuleActionsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |Represents the categories that are stamped on e-mail messages.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifies the ID of the folder that e-mail items will be copied to.  <br/> |
|[Delete](delete.md) <br/> |Indicates whether messages are to be moved to the Deleted Items folder.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Indicates the e-mail addresses to which messages are to be forwarded as attachments.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Indicates the e-mail addresses to which messages are to be forwarded.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Specifies the importance that is to be stamped on messages.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Indicates whether messages are to be marked as read.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifies the ID of the folder that e-mail items will be moved to.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Indicates the e-mail addresses to which messages are to be redirected.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Indicates. the ID of the template message that is to be sent as a reply to incoming messages.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Indicates whether subsequent rules are to be evaluated.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Represents a single rule in a user's mailbox.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [Conditions](conditions.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

