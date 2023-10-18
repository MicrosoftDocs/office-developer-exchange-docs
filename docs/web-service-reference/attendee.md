---
title: "Attendee"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: "The Attendee element represents attendees and resources for a meeting."
---

# Attendee

The **Attendee** element represents attendees and resources for a meeting. 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
   <ProposedStart/>
   <ProposedEnd/>
</Attendee>
```

 **AttendeeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a fully resolved e-mail address.  <br/> |
|[ResponseType](responsetype.md) <br/> |Represents the type of recipient response that is received for a meeting. This property is only relevant to a meeting organizer's calendar item.  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |Represents the date and time of the latest response that is received.  <br/> |
|[ProposedStart](proposedstart-attendeetype.md) <br/> |Represents an attendee's proposed start time for a meeting. <br/> |
|[ProposedEnd](proposedend-attendeetype.md) <br/> |Represents an attendee's proposed end time for a meeting. <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |Represents attendees that are required to attend a meeting.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Represents attendees that are not required to attend a meeting.  <br/> |
|[Resources](resources.md) <br/> |Represents a scheduled resource for a meeting.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

