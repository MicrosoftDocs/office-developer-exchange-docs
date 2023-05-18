---
title: "ProposedEnd (MeetingRegistrationResponseObjectType)"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3e5d2567-a5a2-4791-b209-c29082894a9e
description: "The ProposedEnd (MeetingRegistrationResponseObjectType) element specifies an attendee's proposed new end time for a meeting."
---

# ProposedEnd (MeetingRegistrationResponseObjectType)

The **ProposedEnd (MeetingRegistrationResponseObjectType)** element specifies an attendee's proposed new end time for a meeting. 
  
```XML
<ProposedEnd />
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[AcceptItem](acceptitem.md) | [TentativelyAcceptItem](tentativelyacceptitem.md) | [DeclineItem](declineitem.md)
  
## Text value

The text value of the **ProposedEnd (MeetingRegistrationResponseObjectType)** element is the proposed end date and time of the meeting. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[AcceptItem](acceptitem.md)
  
[DeclineItem](declineitem.md)
  
[TentativelyAcceptItem](tentativelyacceptitem.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

