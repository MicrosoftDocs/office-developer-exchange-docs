---
title: "HasAttachments"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: "The HasAttachments element represents a property that is set to true if an item has at least one visible attachment or if a conversation contains at least one item that has an attachment. This property is read-only."
---

# HasAttachments

The **HasAttachments** element represents a property that is set to **true** if an item has at least one visible attachment or if a conversation contains at least one item that has an attachment. This property is read-only. 
  
```XML
<HasAttachments/>
```

 **Boolean**
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
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Represents a single conversation.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents all the available rule exception conditions for the Inbox rule.  <br/> |
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

A text value that represents a Boolean value is required. A value of **true** means that the item or conversation has at least one visible attachment. A value of **false** means that the item or conversation either has no attachments or has only hidden attachments. 
  
## Remarks

The **HasAttachments** property is calculated from the Boolean **AllAttachmentsHidden** MAPI property. If an item does not have an attachment, the **AllAttachmentsHidden** property does not exist. If all the attachments on the item are hidden, the **AllAttachmentsHidden** property is **true**. The **AllAttachmentsHidden** property is **false** if it has at least one attachment and at least one of the attachments is visible. Use the **AllAttachmentsHidden** MAPI property for searching, grouping, and sorting items. 
  
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

