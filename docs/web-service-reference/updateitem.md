---
title: "UpdateItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: "The UpdateItem element defines a request to update an item in a mailbox."
---

# UpdateItem

The **UpdateItem** element defines a request to update an item in a mailbox. 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ConflictResolution** <br/> |Identifies the type of conflict resolution to try during an update. The default value is AutoResolve.  <br/> |
|**MessageDisposition** <br/> |Describes how the item will be handled after it is updated. The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |Describes how meeting updates are communicated after a calendar item is updated. This attribute is required for calendar items and calendar item occurrences.  <br/> |
|**SuppressReadReceipts** <br/> |Indicates whether read receipts for the updated item should be suppressed. A text value of **true** indicates that read receipts should be suppressed. A value of **false** indicates that the read receipts will be sent to the sender. This attribute is optional.  <br/> This attribute was introduced in Exchange Server 2013 SP1.  <br/> |
   
#### ConflictResolution Attribute

|**Value**|**Description**|
|:-----|:-----|
|NeverOverwrite  <br/> |If there is a conflict, the update operation fails and an error is returned.  <br/> |
|AutoResolve  <br/> |The update operation automatically resolves any conflict.  <br/> |
|AlwaysOverwrite  <br/> |If there is a conflict, the update operation will overwrite information.  <br/> |
   
#### MessageDisposition Attribute

|**Value**|**Description**|
|:-----|:-----|
|SaveOnly  <br/> |The item is updated and saved back to its current folder.  <br/> |
|SendOnly  <br/> |The item is updated and sent but no copy is saved.  <br/> |
|SendAndSaveCopy  <br/> |The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.  <br/> |
   
#### SendMeetingInvitationsOrCancellations Attribute

|**Value**|**Description**|
|:-----|:-----|
|SendToNone  <br/> |The calendar item is updated but updates are not sent to attendees.  <br/> |
|SendOnlyToAll  <br/> |The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.  <br/> |
|SendOnlyToChanged  <br/> |The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.  <br/> |
|SendToAllAndSaveCopy  <br/> |The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.  <br/> |
|SendToChangedAndSaveCopy  <br/> |The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifies the target folder for operations that update, send, and create items in the Exchange store.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.  <br/> |
   
### Parent elements

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

[UpdateItem operation](updateitem-operation.md)

