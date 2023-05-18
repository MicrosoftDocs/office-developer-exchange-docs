---
title: "Item"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: "The Item element represents a generic item in the Exchange store."
---

# Item

The **Item** element represents a generic item in the Exchange store. 
  
```xml
<Item>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Item>
```

 **ItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store. This property is read-only.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the item or folder. This property is read-only.  <br/> |
|[ItemClass](itemclass.md) <br/> |Represents the message class of an item.  <br/> |
|[Subject](subject.md) <br/> |Represents the subject for Exchange store items and response objects. The subject is limited to 255 characters.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indicates the sensitivity level of an item.  <br/> |
|[Body](body.md) <br/> |Represents the actual body content of a message.  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files that are attached to an item in the Exchange store.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Represents the date and time that an item in a mailbox was received.  <br/> |
|[Size](size.md) <br/> |Represents the size in bytes of an item. This property is read-only.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Represents a collection of strings that identify to which categories an item in the mailbox belongs.  <br/> |
|[Importance](importance.md) <br/> |Describes the importance of an item.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Represents the identifier of the item to which this item is a reply.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indicates whether an item has been submitted to the Outbox default folder.  <br/> |
|[IsDraft](isdraft.md) <br/> |Represents whether an item has not yet been sent.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indicates whether a user sent an item to itself.  <br/> |
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
|[HasAttachments](hasattachments.md) <br/> |Represents a property that is set to **true** if an item has attachments at least one visible attachment. This property is read-only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
|[Culture](culture.md) <br/> |Represents the culture for a given item in a mailbox.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contains the display name of the last user to modify an item.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indicates when an item was last modified.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indicates whether the item is associated with a folder.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contains the identifier of an item or conversation.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Represents an HTML fragment or plain text which represents the unique body of this conversation.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describes all calendar items that are adjacent to a meeting time.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifies all items that conflict with a meeting time.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifies a single item to create in the local client store.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[Items](items.md) <br/> |Contains an array of items.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifies a single item to update in the local client store.  <br/> |
   
## Text value

None.
  
## Remarks

It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).
  
[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema. Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements. Microsoft Exchange Server 2010 does not return the base **Item** element in responses. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
  
[EWS reference for Exchange](ews-reference-for-exchange.md)

