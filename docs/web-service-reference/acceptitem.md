---
title: "AcceptItem"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AcceptItem
api_type:
- schema
ms.assetid: 05a15431-77e1-411a-a16b-5481d364d3cc
description: "The AcceptItem element represents an Accept reply to a meeting request."
---

# AcceptItem

The **AcceptItem** element represents an Accept reply to a meeting request. 
  
```xml
<AcceptItem>
   <ItemClass/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <InternetMessageHeaders/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <ProposedStart/>
   <ProposedEnd/>
</AcceptItem>
```

 **AcceptItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemClass](itemclass.md) <br/> |Represents the message class of an item.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indicates the sensitivity level of an item.  <br/> |
|[Body](body.md) <br/> |Represents the actual body content of a message.  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the item or file that is attached to an item in the Exchange store.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Represents the Internet message header name for a given header within the headers collection.  <br/> |
|[Sender](sender.md) <br/> |Identifies the sender of an item.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contains a set of recipients of an item. These are the primary recipients of an item.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Represents a collection of recipients that will receive a copy of the message.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indicates whether the sender of an item requests a read receipt.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indicates whether the sender of an item requests a delivery receipt.  <br/> |
|[ReferenceItemId](referenceitemid.md) <br/> |Identifies the item to which the response object refers.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifies the delegate in a delegate access scenario. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifies the principal in a delegate access scenario. This element was introduced in Exchange 2007 SP1.  <br/> |
|[ProposedStart](proposedstart.md) <br/> |Specifies the proposed start time of the meeting.  <br/> |
|[ProposedEnd](proposedend.md) <br/> |Specifies the proposed end time of the meeting.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> | Describes all items that are adjacent to a meeting time.<br/><br/>  The following are some of the XPath expressions to this element:<br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> | Describes all items that conflict with a meeting time.<br/><br/>  The following are some of the XPath expressions to this element:<br/><br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contains a collection of all the response objects that are associated with an item in the Exchange store.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS directory of the Exchange server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

