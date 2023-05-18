---
title: "ConversationAction"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: "The ConversationAction element contains a single action to be applied to a single conversation."
---

# ConversationAction

The **ConversationAction** element contains a single action to be applied to a single conversation. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 **ConversationActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Action (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element. This element must be present.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation. This element must be present.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Indicates the folder that is targeted for actions that use folders. This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Contains the date and time that a conversation was last synchronized. This element must be present when trying to delete all items in a conversation that were received up to the specified time.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed. This element must be present for the response to be sent asynchronous to the requested action.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indicates the destination folder for copy and move actions.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contains a collection of strings that identify the categories to which items in a conversation belong.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Specifies a flag that enables deletion for all new items in a conversation.  <br/> |
|[IsRead](isread.md) <br/> |Indicates whether a message has been read.  <br/> |
|[DeleteType](deletetype.md) <br/> |Indicates how items in a conversation are deleted.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Contains a collection of conversations and the actions to apply to them.  <br/> |
   
## Text value

**ConversationAction element text values**

|**Value**|**Description**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Always categorize the conversation.  <br/> |
|AlwaysDelete  <br/> |Always delete the conversation.  <br/> |
|AlwaysMove  <br/> |Always move the conversation.  <br/> |
|Delete  <br/> |Delete the conversation.  <br/> |
|Move  <br/> |Move the conversation.  <br/> |
|Copy  <br/> |Copy the conversation.  <br/> |
|SetReadState  <br/> |Set the read state of the conversation.  <br/> |
|SetRetentionPolicy  <br/> |Set the retention policy for the conversation.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ApplyConversationAction operation](applyconversationaction-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

