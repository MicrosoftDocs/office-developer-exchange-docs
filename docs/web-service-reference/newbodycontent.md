---
title: "NewBodyContent"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: "The NewBodyContent element represents the new body content of a message."
---

# NewBodyContent

The **NewBodyContent** element represents the new body content of a message. 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**BodyType** <br/> |Represents the actual body content of a message.  <br/> |
   
#### BodyType Attribute

|**Value**|**Description**|
|:-----|:-----|
|**HTML** <br/> |Converts all bodies to HTML.  <br/> |
|**Text** <br/> |Converts all bodies to plain text.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |Contains a reply to the sender of an item in the Exchange store.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contains a reply to the sender and all identified recipients of an item in the Exchange store.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contains an Exchange store item to forward to recipients.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Represents the response object that is used to cancel a meeting.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contains a reply to a post item. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## Text value

The text value represents the new body content of a message.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

