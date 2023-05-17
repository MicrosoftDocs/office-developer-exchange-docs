---
title: "Items (NonEmptyArrayOfAllItemsType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: "The Items element contains a set of items to create."
---

# Items (NonEmptyArrayOfAllItemsType)

The **Items** element contains a set of items to create. 
  
```XML
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</Items>
```

 **NonEmptyArrayOfAllItemsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange email message.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contains a reply to the sender of an item in the Exchange store.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contains an Exchange store item to forward to recipients.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contains a reply to the sender and all identified recipients of an item in the Exchange store.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Represents an Accept reply to a meeting request.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Represents a Tentative reply to a meeting request.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Represents a Decline reply to a meeting request.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Represents the response object that is used to cancel a meeting.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contains a reply to a post item.  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |Used to suppress read receipts.  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |Used to accept an invitation that allows access to another user's calendar or contacts data.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Defines the request to create an item in the Exchange store.  <br/> The following is the XPath expression to this element:  `/CreateItem` <br/> |
|[ConversationNode](conversationnode.md) <br/> |Identifies a single node in a conversation.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[CreateFolder operation](createfolder-operation.md)
  
[CreateItem operation](createitem-operation.md)


[Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

