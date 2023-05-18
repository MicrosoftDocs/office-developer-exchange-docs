---
title: "From"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- From
api_type:
- schema
ms.assetid: 5a52d644-3677-4049-874c-12bd5c3080dc
description: "The From element represents the address from which the message was sent."
---

# From

The **From** element represents the address from which the message was sent. 
  
```xml
<From>
   <Mailbox/>
</From>
```

 **SingleRecipientType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Represents an Accept reply to a meeting request.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Represents a Tentative reply to a meeting request.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Represents a Decline reply to a meeting request.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contains a reply to the creator of an item in the Exchange store.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contains a reply to all identified recipients of an item in the Exchange store.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contains an Exchange store item to forward to recipients.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Represents the response object that is used to cancel a meeting.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## Remarks

This element is used for "send on behalf of" e-mails.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

