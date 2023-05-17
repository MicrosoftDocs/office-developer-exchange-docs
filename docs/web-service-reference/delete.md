---
title: "Delete"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- schema
ms.assetid: aa45f0c1-a80d-4b6c-8a85-375b6de515f4
description: "The Delete element indicates whether a client can delete a folder or item."
---

# Delete

The **Delete** element indicates whether a client can delete a folder or item. 
  
```XML
<Delete>true or false</Delete>
```

**boolean**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EffectiveRights](effectiverights.md) <br/> |Contains the rights of the client based on the permission settings for the item or folder.  <br/> |
|[Actions](actions.md) <br/> |Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.  <br/> |
   
## Text value

A text value of **true** indicates that a client can delete an item or folder. A value of **false** indicates that a client cannot delete an item or folder. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
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

