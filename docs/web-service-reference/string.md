---
title: "String"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: "The String element represents a string that is used by items, contacts, tasks, and conversations."
---

# String

The **String** element represents a string that is used by items, contacts, tasks, and conversations. 
  
```XML
<String/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contains a collection of strings that identify to which categories an item in the mailbox belongs.  <br/> |
|[Children](children.md) <br/> |Contains the names of the children of a contact.  <br/> |
|[Companies](companies.md) <br/> |Represents the collection of companies that are associated with a contact or task.  <br/> |
|[Contacts](contacts-ex15websvcsotherref.md) <br/> |Contains a list of contacts that are associated with a task.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contains the category list for all conversation items in a mailbox.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contains the recipient list of a conversation aggregated across a mailbox.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contains a list of all the senders of conversation items in the mailbox.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Contains a list of the item classes that must be stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Contains a list of the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contains the list of recipients of the conversation. This element is read-only.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contains a list of all the senders of conversation items in the current folder. This element is read-only.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.  <br/> |
   
## Text value

The text value of this element is a string that represents a category, the child of a contact, a company, a unique recipient of a conversation, or a contact that is associated with a task.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindConversation operation](findconversation-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

