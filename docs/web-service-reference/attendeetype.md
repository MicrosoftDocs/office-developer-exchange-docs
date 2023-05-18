---
title: "AttendeeType"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: "The AttendeeType element represents the type of attendee that is identified in the Email (EmailAddressType) element. This element is used in requests for meeting suggestions."
---

# AttendeeType

The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element. This element is used in requests for meeting suggestions. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## Text value

A text value is required for this element. The following table lists the possible values for this element.
  
|**Value**|**Description**|
|:-----|:-----|
|Organizer  <br/> |The mailbox user and attendee who created the calendar item.  <br/> |
|Required  <br/> |A mailbox user who is a required attendee to the meeting.  <br/> |
|Optional  <br/> |A mailbox user who is an optional attendee to the meeting.  <br/> |
|Room  <br/> |A mailbox entity that represents a room resource used for the meeting.  <br/> |
|Resource  <br/> |A resource such as a TV or projector that is scheduled for use in the meeting.  <br/> |
   
## Remarks

This element is a required child element of the [MailboxData](mailboxdata.md) element. This element can only occur once in the [MailboxData](mailboxdata.md) element. The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
> [!NOTE]
> The AttendeeType schema type is used to represent attendees to a calendar item. Do not confuse this element with elements of the AttendeeType schema type. 
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

