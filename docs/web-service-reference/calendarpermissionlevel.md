---
title: "CalendarPermissionLevel"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: "The CalendarPermissionLevel element represents the permission level that a user has on a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# CalendarPermissionLevel

The **CalendarPermissionLevel** element represents the permission level that a user has on a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 **CalendarPermissionLevelType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The following table lists the possible values for the **CalendarPermissionLevel** element. 
  
**CalendarPermissionLevel element text values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the user has no permissions on the folder.  <br/> |
|Owner  <br/> |Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders. The user is both folder owner and folder contact.  <br/> |
|PublishingEditor  <br/> |Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.  <br/> |
|Editor  <br/> |Indicates that the user can create, read, edit and delete all items in the folder.  <br/> |
|PublishingAuthor  <br/> |Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.  <br/> |
|Author  <br/> |Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.  <br/> |
|NoneditingAuthor  <br/> |Indicates that the user can create and read all items in the folder, and delete only items that the user creates.  <br/> |
|Reviewer  <br/> |Indicates that the user can read all items in the folder.  <br/> |
|Contributor  <br/> |Indicates that the user can create items in the folder. The contents of the folder do not appear.  <br/> |
|FreeBusyTimeOnly  <br/> |Indicates that the user can view only free/busy time within the calendar.  <br/> |
|FreeBusyTimeAndSubjectAndLocation  <br/> |Indicates that the user can view free/busy time within the calendar and the subject and location of appointments.  <br/> |
|Custom  <br/> |Indicates that the user has custom access permissions on the folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

