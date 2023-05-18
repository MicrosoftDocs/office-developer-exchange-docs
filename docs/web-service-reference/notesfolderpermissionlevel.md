---
title: "NotesFolderPermissionLevel"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- NotesFolderPermissionLevel
api_type:
- schema
ms.assetid: 76a2520c-f453-4fd7-b3eb-1c5f4666680a
description: "The NotesFolderPermissionLevel element contains the permissions for the default Notes folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# NotesFolderPermissionLevel

The **NotesFolderPermissionLevel** element contains the permissions for the default Notes folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<NotesFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</NotesFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
 
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md)|Contains the delegate permission level settings for a user. This element was introduced in Exchange 2007 SP1. |
   
## Text value

The following table lists the text values that represent the permission levels.
  
**Permission level text values**

|**Permission level**|**Description**|
|:-----|:-----|
|None |The delegate user has no access permissions to the Notes folder. |
|Reviewer |The delegate user can read items in the Notes folder. |
|Author |The delegate user can read and create items in the Notes folder. |
|Editor |The delegate user can read, create, and modify items in the Notes folder. |
|Custom |The delegate user has custom access permissions to the Notes folder. |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace |https://schemas.microsoft.com/exchange/services/2006/types |
|Schema Name |Types schema |
|Validation File |Types.xsd |
|Can be Empty |False |
   
## See also



[AddDelegate operation](adddelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

