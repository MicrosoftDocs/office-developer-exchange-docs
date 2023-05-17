---
title: "Permission"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: "The Permission element defines the access that a user has to a folder."
---

# Permission

The **Permission** element defines the access that a user has to a folder. 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **PermissionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |Indicates whether a user has permission to create items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Indicates whether a user has permission to create subfolders in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Indicates whether a user has permission to delete items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[EditItems](edititems.md) <br/> |Indicates whether a user has permission to edit items in a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Indicates whether a user is a contact for a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Indicates whether a user is the owner of a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Indicates whether a user can view a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |Represents the combination of permissions that a user has on a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Indicates whether a user has permission to read items within a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[UserId](userid.md) <br/> |Identifies a delegate user or a user who has folder access permissions. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Permissions](permissions.md) <br/> |Contains all the configured permissions for a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).
  
### Version differences

For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request. To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

