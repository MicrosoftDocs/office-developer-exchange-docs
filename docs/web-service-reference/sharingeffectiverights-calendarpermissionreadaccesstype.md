---
title: "SharingEffectiveRights (CalendarPermissionReadAccessType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: "The SharingEffectiveRights element indicates the permissions that the user has for the calendar data that is being shared."
---

# SharingEffectiveRights (CalendarPermissionReadAccessType)

The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared. 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 **CalendarPermissionReadAccessType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Represents a folder that primarily contains calendar items.  <br/> |
   
## Text value

The following table lists the possible values for the **SharingEffectiveRights** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the user does not have permission to view items in the calendar.  <br/> |
|TimeOnly  <br/> |Indicates that the user has permission to view only free/busy time in the calendar.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.  <br/> |
|FullDetails  <br/> |Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
