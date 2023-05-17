---
title: "Size"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Size
api_type:
- schema
ms.assetid: 966f4daf-c20e-49f8-aeb6-965f3e2da7c3
description: "The Size element represents the size in bytes of an item or all the items in a conversation in the current folder. This property is read-only."
---

# Size

The **Size** element represents the size in bytes of an item or all the items in a conversation in the current folder. This property is read-only. 
  
```XML
<Size/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Represents a single conversation.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Represents a file that is attached to an item in the Exchange store.  <br/> |
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

The text value is an integer value that identifies the size of the item in bytes.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Code**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

