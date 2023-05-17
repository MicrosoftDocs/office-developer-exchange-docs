---
title: "IsFolderOwner"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsFolderOwner
api_type:
- schema
ms.assetid: 6541ee78-d6e6-42a7-8e7a-d8736172b245
description: "The IsFolderOwner element indicates whether a user is the owner of a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# IsFolderOwner

The **IsFolderOwner** element indicates whether a user is the owner of a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<IsFolderOwner/>
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
|[Permission](permission.md) <br/> |Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

A text value of **true** indicates that the user is the owner of the folder. A value of **false** indicates that the user is not the owner of the folder. 
  
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

