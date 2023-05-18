---
title: "FindConversation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: "The FindConversation element defines a request to find conversations in a mailbox."
---

# FindConversation

The **FindConversation** element defines a request to find conversations in a mailbox. 
  
[FindConversation](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 **FindConversationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

****

|**Attribute**|**Description**|
|:-----|:-----|
|Traversal  <br/> |Identifies the types of sub-tree traversal. This attribute is optional.  <br/> |
|ViewFilter  <br/> |Identifies the types view filters. This attribute is optional.  <br/> |
   
#### Traversal attribute values

****

|**Value**|**Description**|
|:-----|:-----|
|Shallow  <br/> |Indicates a shallow traversal.  <br/> |
|Deep  <br/> |Indicates a deep traversal.  <br/> |
   
#### ViewFilter attribute values

****

|**Value**|**Description**|
|:-----|:-----|
|All  <br/> |Find all conversations.  <br/> |
|Flagged  <br/> |Find flagged conversations.  <br/> |
|HasAttachment  <br/> |Find conversations with attachments.  <br/> |
|ToOrCcMe  <br/> |Find conversations addressed or cc'd to me.  <br/> |
|Unread  <br/> |Find unread conversations.  <br/> |
|TaskActive  <br/> |Find active tasks.  <br/> |
|TaskOverdue  <br/> |Find overdue tasks.  <br/> |
|TaskCompleted  <br/> |Find completed tasks.  <br/> |
|NoClutter  <br/> |For internal use only.  <br/> |
|Clutter  <br/> |For internal use only.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describes how paged conversation information is returned.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.  <br/> |
|[SortOrder](sortorder.md) <br/> |Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request. The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifies the folder to search for conversations.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Specifies a mailbox query string based on Advanced Query Syntax (AQS).  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindConversation operation](findconversation-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

