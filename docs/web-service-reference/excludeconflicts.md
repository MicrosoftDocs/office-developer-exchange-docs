---
title: "ExcludeConflicts"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExcludeConflicts
api_type:
- schema
ms.assetid: ec33ef23-8537-41eb-8d89-7eb906a1fad7
description: "The ExcludeConflicts element specifies whether to return suggested times for calendar times that conflict among the attendees."
---

# ExcludeConflicts

The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[MailboxDataArray](mailboxdataarray.md)
  
[MailboxData](mailboxdata.md)
  
[ExcludeConflicts](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
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
|[MailboxData](mailboxdata.md) <br/> |Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## Text value

A text value is required. The possible values are a Boolean **true** or **false**.
  
## Remarks

This element is required.
  
> [!NOTE]
> The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserAvailability operation](getuseravailability-operation.md)
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

