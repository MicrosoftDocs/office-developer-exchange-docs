---
title: "MeetingMessage"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MeetingMessage
api_type:
- schema
ms.assetid: c95956a8-7505-44b4-bea4-11d1f5182796
description: "The MeetingMessage element represents a meeting in the Exchange store."
---

# MeetingMessage

The **MeetingMessage** element represents a meeting in the Exchange store. 
  
```xml
<MeetingMessage>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</MeetingMessage>
```

 **MeetingMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contains the native MIME stream of an object that is represented in base64Binary format.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store. This property is read-only.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the item or folder. This property is read-only.  <br/> |
|[ItemClass](itemclass.md) <br/> |Represents the message class of an item.  <br/> |
|[Subject](subject.md) <br/> |Represents the subject for Exchange store items and response objects. The subject is limited to 255 characters.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Contains the status for an item's sensitivity.  <br/> |
|[Body](body.md) <br/> |Represents the actual body content of a message.  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files that are attached to an item in the Exchange store.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Represents the date and time that an item in a mailbox was received.  <br/> |
|[Size](size.md) <br/> |Represents the size in bytes of an item. This property is read-only.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Represents a collection of strings that identify to which categories an item in the mailbox belongs.  <br/> |
|[Importance](importance.md) <br/> |Describes the importance of an item.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Represents the identifier of the item to which this item is a reply.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indicates whether an item has been submitted to the Outbox default folder.  <br/> |
|[IsDraft](isdraft.md) <br/> |Represents whether an item has not yet been sent.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indicates whether a user sent an item to him or herself.  <br/> |
|[IsResend](isresend.md) <br/> |Indicates whether the item had previously been sent.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indicates whether the item has been modified.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Represents the collection of all Internet message headers that are contained within an item in a mailbox.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Represents the date and time that an item in a mailbox was sent.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Represents the date and time that a given item in the mailbox was created.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contains a collection of all the response objects that are associated with an item in the Exchange store.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Represents the date and time when the event occurs. This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indicates whether a reminder has been set for an item in the Exchange store.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Represents the number of minutes before an event when a reminder is displayed.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Represents the display string that is used for the contents of the Cc box. This is the concatenated string of all Cc recipient display names.  <br/> |
|[DisplayTo](displayto.md) <br/> |Represents the display string that is used for the contents of the To box. This is the concatenated string of all To recipient display names.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Represents a property that is set to **true** if an item has at least one visible attachment. This property is read only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
|[Culture](culture.md) <br/> |Represents the culture for a given item in a mailbox.  <br/> |
|[Sender](sender.md) <br/> |Identifies the sender of an item.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contains a set of recipients of a message.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Represents a collection of recipients that will receive a copy of the message.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indicates whether the sender of an item requests a read receipt.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indicates whether the sender of an item requests a delivery receipt.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contains a binary ID that represents the thread to which this message belongs.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Represents the conversation identifier.  <br/> |
|[From](from.md) <br/> |Represents the addressee from whom the message was sent.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Represents the Internet message identifier of an item.  <br/> |
|[IsRead](isread.md) <br/> |Indicates whether a message has been read.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indicates whether a response to an e-mail message is requested.  <br/> |
|[References](references.md) <br/> |Represents the Usenet header that is used to correlate replies with their original messages.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifies a set of addresses to which replies should be sent.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Indicates whether a meeting was handled by an account with delegate access.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Indicates whether a meeting message is out-of-date.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Indicates whether a meeting message item has been processed.  <br/> |
|[ResponseType](responsetype.md) <br/> |Represents the type of recipient response received for a meeting.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifies the delegate in a delegate access scenario.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifies the principal in a delegate access scenario.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contains the display name of the last user to modify an item.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indicates when an item was last modified.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indicates whether the item is associated with a folder.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contains the identifier of an item or conversation.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Represents an HTML fragment or plain text which represents the unique body of this conversation.  <br/> |
|[UID](uid.md) <br/> |Identifies a calendar item.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Used to identify a specific instance of a recurring calendar item.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Indicates the date and time that an instance of an iCalendar object was created.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describes all calendar items that are adjacent to a meeting time.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifies all items that conflict with a meeting time.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifies a single item to create in the local client store.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifies a single item to update in the local client store.  <br/> |
|[Items](items.md) <br/> |Contains an array of items.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

