---
title: "StoreEntryId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f536e264-8c4d-4cc5-bab8-22a4fa38de39
description: "The StoreEntryId element contains the Exchange store identifier of an item."
---

# StoreEntryId

The **StoreEntryId** element contains the Exchange store identifier of an item. 
  
```XML
<StoreEntryId/>
```

 **xs:base64Binary**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |Represents an accept reply to a meeting request.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.  <br/> |
|[Contact](contact.md) <br/> |Represents a contact item in the Exchange store.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Represents a decline reply to a meeting request.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents all the available rule exception conditions for an Inbox rule.  <br/> |
|[Item](item.md) <br/> |Represents a generic Exchange item.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Represents a tentatively accepted reply to a meeting request.  <br/> |
   
## Text value

The text value is a string that represents the store item identifier.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

|**Name**|**Value**
|:-----|:-----|
|Namespace  <br/> |
|Schema Name  <br/> |
|Validation File  <br/> |
|Can be Empty  <br/> |
   

