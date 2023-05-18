---
title: "ReceiveCopiesOfMeetingMessages"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: "The ReceiveCopiesOfMeetingMessages element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# ReceiveCopiesOfMeetingMessages

The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
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
|[DelegateUser](delegateuser.md) <br/> |Identifies a single delegate to add or update in a mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

A text value of **true** indicates that a delegate receives a copy of meeting messages. A text value of **false** indicates that a delegate does not receive a copy of meeting messages. 
  
## Remarks

When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[AddDelegate operation](adddelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

