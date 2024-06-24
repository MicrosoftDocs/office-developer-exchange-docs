---
title: "InboxFolderPermissionLevel"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InboxFolderPermissionLevel
api_type:
- schema
ms.assetid: f250d31b-9193-4c1c-8350-900dead3a023
description: "The InboxFolderPermissionLevel element contains the permissions for the default Inbox folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# InboxFolderPermissionLevel

The **InboxFolderPermissionLevel** element contains the permissions for the default Inbox folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<InboxFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</InboxFolderPermissionLevel>
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
|[DelegatePermissions](delegatepermissions.md) <br/> |Contains the delegate permission level settings for a user. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The following table lists the text values that represent the permission levels.
  
**Permission level text values**

|**Permission level**|**Description**|
|:-----|:-----|
|None  <br/> |The delegate user has no access permissions to the Inbox folder.  <br/> |
|Reviewer  <br/> |The delegate user can read items in the Inbox folder.  <br/> |
|Author  <br/> |The delegate user can read and create items in the Inbox folder.  <br/> |
|Editor  <br/> |The delegate user can read, create, and modify items in the Inbox folder.  <br/> |
|Custom  <br/> |The delegate user has custom access permissions to the Inbox folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[AddDelegate operation](adddelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

