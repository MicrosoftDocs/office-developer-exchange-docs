---
title: "CalendarPermission"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: "The CalendarPermission element defines the access that a user has to a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# CalendarPermission

The **CalendarPermission** element defines the access that a user has to a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **CalendarPermissionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarPermissionLevel](calendarpermissionlevel.md) <br/> |Represents the permission level that a user has on a Calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[CanCreateItems](cancreateitems.md) <br/> |Indicates whether a user has permission to create items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Indicates whether a user has permission to create subfolders in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Indicates whether a user has permission to delete items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[EditItems](edititems.md) <br/> |Indicates whether a user has permission to edit items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Indicates whether a user is a contact for a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Indicates whether a user is the owner of a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Indicates whether a user can view a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[ReadItems (CalendarPermissionType)](readitems-calendarpermissiontype.md) <br/> |Indicates whether a user has permission to read items within a calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[UserId](userid.md) <br/> |Identifies a delegate user or a user who has folder access permissions. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |Contains an array of calendar permissions for a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

