---
title: "EditItems"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EditItems
api_type:
- schema
ms.assetid: 1cb14493-c999-4d66-b82c-ecb410dc1c00
description: "The EditItems element indicates which items in a folder a user has permission to edit. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# EditItems

The **EditItems** element indicates which items in a folder a user has permission to edit. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<EditItems>None or Owned or All</EditItems>
```

 **PermissionActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Permission](permission.md) <br/> |Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The following table lists the possible values for the **EditItems** element. 
  
**EditItems element text values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the user does not have permission to edit items in the folder.  <br/> |
|Owned  <br/> |Indicates that the user has permission to edit the items that the user owns in the folder.  <br/> |
|All  <br/> |Indicates that the user has permission to edit all items in the folder.  <br/> |
   
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
- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

