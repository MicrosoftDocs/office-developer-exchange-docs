---
title: "ParentFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: "The ParentFolderId element represents the identifier of the parent folder that contains the item or folder."
---

# ParentFolderId

The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder. 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Contains a string that identifies a folder in the Exchange store. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Contains a string that identifies a version of a folder that is identified by the **Id** attribute. This attribute is optional. Use this attribute to make sure that the correct version of a folder is used.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Represents a calendar folder in a mailbox.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents a calendar item in a mailbox.  <br/> |
|[Contact](contact.md) <br/> |Represents a contact item in a mailbox.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contacts folder in a mailbox.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Represents an event in which an item or folder is copied.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Represents an event in which an item or folder is created.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Represents an event in which an item or folder is deleted.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a private distribution list in a mailbox.  <br/> |
|[Folder](folder.md) <br/> |Represents a folder in a mailbox.  <br/> |
|[Item](item.md) <br/> |Represents a generic Exchange item.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Represents a single item to upload into a mailbox.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in a mailbox.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message in a mailbox.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in a mailbox.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in a mailbox.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an e-mail message in a mailbox.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Represents an event in which an item or folder is modified.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event in which an item or folder is moved from one parent folder to another parent folder.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Represents an event that is triggered by a new mail item in a mailbox.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Represents an Accept reply to a meeting request.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Represents a Tentative reply to a meeting request.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Represents a Decline reply to a meeting request.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task item in a mailbox.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contains a reply to the creator of an item in the Exchange store.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contains a reply to all identified recipients of an item in the Exchange store.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contains an Exchange store item to forward to recipients.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Represents the response object that is used to cancel a meeting.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a task folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder in a mailbox.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

