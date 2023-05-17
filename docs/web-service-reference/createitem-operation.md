---
title: "CreateItem operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: "The CreateItem operation creates items in the Exchange store."
---

# CreateItem operation

The CreateItem operation creates items in the Exchange store.
  
## Using the CreateItem Operation

You can use the CreateItem operation to create the following:
  
- Calendar items
    
- E-mail messages
    
- Meeting requests
    
- Tasks
    
- Contacts
    
For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).
  
The CreateItem operation supports the use of response objects. Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message. The following table lists the response objects that are handled in the CreateItem operation.
  
|**Response object**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |Accept a meeting request.  <br/> |
|CancelCalendarItem  <br/> |Cancel a meeting. This differs from deleting all attendees because it deletes the meeting for the organizer also.  <br/> |
|DeclineItem  <br/> |Decline a meeting request.  <br/> |
|ForwardItem  <br/> |Send a meeting request to another person as a meeting request.  <br/> |
|RemoveItem  <br/> |Remove a canceled meeting from the calendar.  <br/> |
|ReplyAllToItem  <br/> |Send a message that includes the body of the original meeting request to all attendees of the meeting.  <br/> |
|ReplyToItem  <br/> |Send a message that includes the body of the original meeting request to the sender of the meeting request.  <br/> |
|SendReadReceipt  <br/> |Send a read receipt to the sender of the meeting request.  <br/> |
|TentativelyAcceptItem  <br/> |Tentatively accept a meeting request.  <br/> |
   
The CreateItem operation also supports additional meeting objects. The following table lists additional objects that the CreateItem operation supports.
  
|**Meeting object**|**Description**|
|:-----|:-----|
|Meeting Message  <br/> |Represents a meeting message in the Exchange store. This is the base object for the other meeting objects.  <br/> |
|Meeting Request  <br/> |Represents a meeting request in the Exchange store.  <br/> |
|Meeting Response  <br/> |Represents a meeting response in the Exchange store.  <br/> |
|Meeting Cancellation  <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
   
## See also



[CreateItem operation (calendar item)](createitem-operation-calendar-item.md)
  
[CreateItem operation (contact)](createitem-operation-contact.md)
  
[CreateItem operation (email message)](createitem-operation-email-message.md)
  
[CreateItem operation (meeting request)](createitem-operation-meeting-request.md)
  
[CreateItem operation (task)](createitem-operation-task.md)
  
 **CreateItemType**

