---
title: "PermissionSet (PermissionSetType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: "The PermissionSet element contains all the permissions that are configured for a folder."
---

# PermissionSet (PermissionSetType)

The **PermissionSet** element contains all the permissions that are configured for a folder. 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **PermissionSetType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Permissions](permissions.md) <br/> |Contains the collection of permissions for a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Contains an array of unknown entries that cannot be resolved against the Active Directory directory service. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Defines a folder to create, get, find, synchronize, or update.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder that is contained in a mailbox.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contacts folder that is contained in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a tasks folder that is contained in a mailbox.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).
  
### Version differences

For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request. To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request. 
  
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

