---
title: "Attendees"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: "The Attendees element specifies the recipients of an invitation to a meeting."
---

# Attendees

The **Attendees** element specifies the recipients of an invitation to a meeting. 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 **ArrayOfEmailUsersType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[EmailUser](emailuser.md) <br/> |Specifies an email recipient or Active Directory contact.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MeetingSuggestion](meetingsuggestion.md) <br/> |Specifies a proposed meeting.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

