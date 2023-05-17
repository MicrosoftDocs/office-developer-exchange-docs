---
title: "SharingEffectiveRights (PermissionReadAccessType)"
 
 
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
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: "The SharingEffectiveRights element indicates the permissions that the user has for the contact data that is being shared."
---

# SharingEffectiveRights (PermissionReadAccessType)

The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared. 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 **PermissionReadAccessType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ContactsFolder](contactsfolder.md) <br/> |Represents a Contacts folder that is contained in a mailbox.  <br/> |
   
## Text value

The following table lists the possible values for the **SharingEffectiveRights** element. 
  
**SharingEffectiveRights element text values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the user does not have permission to read items in the folder.  <br/> |
|FullDetails  <br/> |Indicates that the user has permission to read all items in the folder.  <br/> |
   
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

