---
title: "MailboxData"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: "The MailboxData element represents an individual mailbox user and options for the type of data to be returned about the mailbox user."
---

# MailboxData

The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

**MailboxData**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Email (EmailAddressType)](email-emailaddresstype.md) <br/> |Represents the mailbox user for a GetUserAvailability query.  <br/> |
|[AttendeeType](attendeetype.md) <br/> |Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element. This is used in requests for meeting suggestions.  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |Specifies whether to return suggested times for calendar times that conflict among the attendees.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |Contains a list of mailboxes to query for availability information.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## Remarks

A client application can define one to many **MailboxData** elements. 
  
> [!NOTE]
> The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed. 
  
## Example

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

