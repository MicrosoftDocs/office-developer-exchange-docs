---
title: "Conversation (ConversationType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: "The Conversation element represents a single conversation."
---

# Conversation (ConversationType)

The **Conversation** element represents a single conversation. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[Conversation (ConversationType)](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 **ConversationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |Represents the identifier of a conversation.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Represents the conversation topic. This element is read-only.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contains the recipient list of a conversation aggregated from a particular folder. This element is read-only.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contains the recipient list of a conversation aggregated across a mailbox. This element is read-only.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder. This element is read-only.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contains a list of all the senders of conversation items in the current folder. This element is read-only.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contains a list of all the senders of conversation items in the mailbox.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Contains the delivery time of the message that was last received in this conversation in the current folder.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contains the category list for all conversation items in a mailbox.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Contains the aggregated flag status for conversation items in the current folder.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Contains the aggregated flag status for all conversation items in a mailbox.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Contains a value that indicates whether at least one conversation item in the current folder has an attachment.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.  <br/> |
|[MessageCount](messagecount.md) <br/> |Contains the total number of conversation items in the current folder.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Contains the total number of conversation items in the mailbox.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Contains the count of unread conversation items within a folder.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Contains a count of all the unread conversation items in the mailbox.  <br/> |
|[Size](size.md) <br/> |Contains the conversation size calculated from the size of all conversation items in the current folder.  <br/> |
|[GlobalSize](globalsize.md) <br/> |Contains the size of the conversation calculated from the size of all conversation items in the mailbox.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Contains a list of item classes that represents all the item classes of the conversation items in the current folder.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.  <br/> |
|[Importance](importance.md) <br/> |Contains the aggregated importance for all conversation items in the current folder.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Contains the aggregated importance for all conversation items in a mailbox.  <br/> |
|[ItemIds](itemids.md) <br/> |Contains the collection of item identifiers for all conversation items in the current folder.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contains the collection of item identifiers for all conversation items in a mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conversations](conversations-ex15websvcsotherref.md) <br/> |Contains an array of conversations that are returned in the **FindConversation** response.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[FindConversation operation](findconversation-operation.md)
  
[ApplyConversationAction operation](applyconversationaction-operation.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

