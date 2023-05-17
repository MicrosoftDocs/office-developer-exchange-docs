---
title: "IsRead"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsRead
api_type:
- schema
ms.assetid: 161455d5-a870-4c99-b2eb-c759c538f1bc
description: "The IsRead element indicates whether a message has been read."
---

# IsRead

The **IsRead** element indicates whether a message has been read. 
  
```XML
<IsRead/>
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
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[ConversationAction](conversationaction.md) <br/> |Contains a single action to be applied to a single conversation.  <br/> |
   
## Text value

A text value of **true** indicates that the message has been read. A text value of **false** indicates that the message has not been read. 
  
## Remarks

If [IsReadReceiptRequested](isreadreceiptrequested.md) is **true**, setting **IsRead** to **true** sends a read receipt. The recipient can suppress read receipts by submitting the [SuppressReadReceipt](suppressreadreceipt.md) response object before setting the **IsRead** property. 
  
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

