---
title: "ItemId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: "The ItemId element contains the unique identifier and change key of an item in the Exchange store."
localization_priority: Priority
---

# ItemId

The **ItemId** element contains the unique identifier and change key of an item in the Exchange store. 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Identifies a specific item in the Exchange store. **Id** is case-sensitive; therefore, comparisons between **Ids** must be case-sensitive or binary.  <br/> |
|**ChangeKey** <br/> | Identifies a specific version of an item. <br/><br/>A **ChangeKey** is required for the following scenarios: <br/> <br/>- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve. AutoResolve is a default value. If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.  <br/><br/>- The [SendItem](senditem.md) element requires a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item. If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Represents an event when an item or folder is copied.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Represents an event when an item or folder is created.  <br/> |
|[Delete (ItemSync)](delete-itemsync.md) <br/> |Identifies a single item to delete in the local client store.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Represents an event when an item or folder is deleted.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contains the status and results of a request to export a single mailbox item.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Represents the first occurrence of a recurring calendar item.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contains the collection of item identifiers for all conversation items in a mailbox.  <br/> |
|[Ignore](ignore.md) <br/> |Identifies items to skip during synchronization.  <br/> |
|[Item](item.md) <br/> |Represents a generic Exchange item.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Represents a single item to upload into a mailbox.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contains an item identifier and the updates to apply to the item.  <br/><br/> The following is the XPath expression to this element: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Contains the unique identities of items, occurrence items, and recurring master items used to delete, send, get, move, or copy items in the Exchange store. <br/> <br/>  The following are the XPath expressions to this element: <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |Contains an array of item identifiers that identify the items to export from a mailbox.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Represents the last occurrence of a recurring calendar item.  <br/> |
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Represents an event that occurs when an item is modified.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event that occurs when an item is moved from one parent folder to another parent folder.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Represents an event that is triggered by a new mail item in a mailbox.  <br/> |
|[Occurrence](occurrence.md) <br/> |Represents a single modified occurrence of a recurring calendar item.  <br/> |
|[PlayOnPhone (Exchange Web Services)](playonphone-exchange-web-services.md) <br/> |Represents a request to read an item on a telephone.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[RoomList](roomlist.md) <br/> |Represents an e-mail address that identifies a list of meeting rooms.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contains the status and results of a request to upload a single mailbox item.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Defines a single user configuration object.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ExportItems operation](exportitems-operation.md)
- [UploadItems operation](uploaditems-operation.md) 
- [FindConversation operation](findconversation-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
