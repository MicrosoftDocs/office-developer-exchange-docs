---
title: "CalendarItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CalendarItem
api_type:
- schema
ms.assetid: b0c1fd27-b6da-46e5-88b8-88f00c71ba80
description: "The CalendarItem element represents an Exchange calendar item."
---

# CalendarItem

The **CalendarItem** element represents an Exchange calendar item. 
  
```XML
<CalendarItem>
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
   <Start/>
   <End/>
   <OriginalStart/>
   <IsAllDayEvent/>
   <LegacyFreeBusyStatus/>
   <Location/>
   <When/>
   <IsMeeting/>
   <IsCancelled/>
   <IsRecurring/>
   <MeetingRequestWasSent/>
   <IsResponseRequested/>
   <CalendarItemType/>
   <MyResponseType/>
   <Organizer/>
   <RequiredAttendees/>
   <OptionalAttendees/>
   <Resources/>
   <ConflictingMeetingCount/>
   <AdjacentMeetingCount/>
   <ConflictingMeetings/>
   <AdjacentMeetings/>
   <Duration/>
   <TimeZone/>
   <AppointmentReplyTime/>
   <AppointmentSequenceNumber/>
   <AppointmentState/>
   <Recurrence/>
   <FirstOccurrence/>
   <LastOccurrence/>
   <ModifiedOccurrences/>
   <DeletedOccurrences/>
   <MeetingTimeZone/>
   <StartTimeZone/>
   <EndTimeZone/>
   <ConferenceType/>
   <AllowNewTimeProposal/>
   <IsOnlineMeeting/>
   <MeetingWorkspaceUrl/>
   <NetShowUrl/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</CalendarItem>
```

 **CalendarItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the item or folder.  <br/> |
|[ItemClass](itemclass.md) <br/> |Represents the message class of an item.  <br/> |
|[Subject](subject.md) <br/> |Represents the subject for Exchange store items and response objects.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indicates the sensitivity level of an item.  <br/> |
|[Body](body.md) <br/> |Represents the actual body content of a message.  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files that are attached to an item in the Exchange store.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Represents the date and time that an item in a mailbox was received.  <br/> |
|[Size](size.md) <br/> |Represents the size in bytes of an item. This property is read-only.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Represents a collection of strings that identify the categories to which an item in the mailbox belongs.  <br/> |
|[Importance](importance.md) <br/> |Describes the importance of an item.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Represents the identifier of the item to which this item is a reply.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indicates whether an item has been submitted to the Outbox default folder.  <br/> |
|[IsDraft](isdraft.md) <br/> |Indicates whether an item has not yet been sent.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indicates whether a user sent an item to him or herself.  <br/> |
|[IsResend](isresend.md) <br/> |Indicates whether the item had previously been sent.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indicates whether the item has been modified.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Represents the collection of all Internet message headers that are contained in an item in a mailbox.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Represents the date and time that an item in a mailbox was sent.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Represents the date and time that a given item in the mailbox was created.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contains a collection of all the response objects that are associated with an item in the Exchange store.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Represents the date and time when the event occurs. This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indicates whether a reminder has been set for an item in the Exchange store.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Represents the number of minutes before an event when a reminder is displayed.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Represents the display string that is used for the contents of the Cc line. This is the concatenated string of all Cc recipient display names.  <br/> |
|[DisplayTo](displayto.md) <br/> |Represents the display string that is used for the contents of the To line. This is the concatenated string of all To recipient display names.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Represents a property that is set to **true** if an item has at least one visible attachment. This property is read-only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
|[Culture](culture.md) <br/> |Represents the culture for a given item in a mailbox.  <br/> |
|[UID](uid.md) <br/> |Identifies a calendar item.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Used to identify a specific instance of a recurring calendar item.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Indicates the date and time that an instance of a iCalendar object was created.  <br/> |
|[Start](start.md) <br/> |Represents the start of a calendar item. This element only applies to a single occurrence of a calendar item.  <br/> |
|[End ](end-ex15websvcsotherref.md) <br/> |Represents the end of a duration. This element only applies to a single occurrence of a calendar item.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Represents the original start time of a calendar item.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Indicates whether a calendar item or meeting request represents an all-day event.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Represents the free/busy status of the calendar item.  <br/> |
|[Location](location.md) <br/> |Represents the location of a meeting or appointment.  <br/> |
|[When](when.md) <br/> |Provides information about when a calendar item occurs.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Indicates whether the calendar item is a meeting or appointment.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Indicates whether an appointment or meeting has been canceled.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Indicates whether a calendar item is part of a recurring item. This element is read-only.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Indicates whether a meeting request has been sent to requested attendees.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indicates whether a response to an item is required.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Represents the occurrence type of a calendar item.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Contains the status of or response to a calendar item.  <br/> |
|[Organizer](organizer.md) <br/> |Represents the organizer of a meeting.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Represents attendees that are required to attend a meeting.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Represents attendees that are not required to attend a meeting.  <br/> |
|[Resources](resources.md) <br/> |Represents a scheduled resource for a meeting.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Represents the number of meetings that conflict with the calendar item.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Represents the total number of calendar items that are adjacent to a meeting time.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifies all items that conflict with a meeting time.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describes all calendar items that are adjacent to a meeting time.  <br/> |
|[Duration (Items)](duration-items.md) <br/> |Represents the duration of a calendar item.  <br/> |
|[TimeZone (Item)](timezone-item.md) <br/> |Provides a text description of a time zone.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Represents the date and time when an attendee replied to a meeting request.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Specifies the sequence number of a version of an appointment.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Specifies the status of the appointment.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contains the recurrence pattern for calendar items and meeting requests.  <br/> This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Represents the first occurrence of a recurring calendar item.  <br/> This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Represents the last occurrence of a recurring calendar item.  <br/> This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contains an array of recurring calendar item occurrences that have been modified so that they differ from the recurrence master item.  <br/> This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Contains an array of deleted occurrences of a recurring calendar item.  <br/> This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Represents the time zone of the location where the meeting is hosted.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Represents the start time zone of the calendar item.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Represents the end time zone of the calendar item.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Describes the type of conferencing that is performed with a calendar item.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Indicates whether a new meeting time can be proposed for a meeting by an attendee.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Indicates whether the meeting is online.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Contains the URL for the meeting workspace that is linked to by the calendar item.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Specifies the URL for a Microsoft NetShow online meeting.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contains the display name of the last user to modify an item.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indicates when an item was last modified.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indicates whether the item is associated with a folder.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to edit an item in Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contains the identifier of an item or conversation.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Represents an HTML fragment or plain text which represents the unique body of this conversation.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describes all calendar items that are adjacent to a meeting time.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifies all items that conflict with a meeting time.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifies a single folder to create in the local client store.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[Items](items.md) <br/> |Contains an array of items.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifies a single item to update in the local client store.  <br/> |
   
## Text value

None.
  
## Remarks

When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) element must be specified in order to preserve the calendar item's original time zone. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
  
[EWS reference for Exchange](ews-reference-for-exchange.md)

