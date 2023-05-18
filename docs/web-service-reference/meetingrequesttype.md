---
title: "MeetingRequestType"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: "The MeetingRequestType element describes the type of the meeting request."
---

# MeetingRequestType

The **MeetingRequestType** element describes the type of the meeting request. 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
   
## Text value

A text value is required. The following table lists the possible text values for this element.
  
|**Value**|**Description**|
|:-----|:-----|
|FullUpdate  <br/> |Identifies the meeting request as a full update to an existing request. A full update has updated time and informational content.  <br/> |
|InformationalUpdate  <br/> |Identifies the meeting request as only containing updated informational content.  <br/> |
|NewMeetingRequest  <br/> |Identifies the meeting request as a new meeting request.  <br/> |
|None  <br/> |Indicates that the meeting request type is not defined.  <br/> |
|Outdated  <br/> |Identifies the meeting request as outdated.  <br/> |
|PrincipalWantsCopy  <br/> |Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.  <br/> |
|SilentUpdate  <br/> |Identifies the meeting request as a silent update to an existing meeting.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

