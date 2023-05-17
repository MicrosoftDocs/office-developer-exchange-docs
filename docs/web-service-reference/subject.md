---
title: "Subject"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Subject
api_type:
- schema
ms.assetid: c140d6c2-deb1-4f67-a908-9397197c4ae7
description: "The Subject element represents the subject property of Exchange store items. The subject is limited to 255 characters."
---

# Subject

The **Subject** element represents the subject property of Exchange store items. The subject is limited to 255 characters. 
  
```XML
<Subject/>
```

 **string**
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
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Represents a cancel calendar item response object.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Specifies criteria for the types of messages to find.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Represents a forward item smart response object.  <br/> |
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an e-mail in the Exchange store.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Represents a remove item response object.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Represents a reply-to-all smart response object.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Represents a reply-to-item smart response object.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

A text value that contains the subject of an Exchange item is required.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

