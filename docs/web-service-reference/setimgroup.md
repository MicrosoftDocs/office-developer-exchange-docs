---
title: "SetImGroup"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c107b8d-714b-4cd5-ad1b-97b7cbcb90d6
description: "The SetImGroup element represents a request to change the display name of an instant messaging group."
---

# SetImGroup

The **SetImGroup** element represents a request to change the display name of an instant messaging group. 
  
```XML
<SetImGroup>
   <GroupId/>
   <NewDisplayName/>
</SetImGroup>
```

 **SetImGroupType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[GroupId](groupid.md) | [NewDisplayName](newdisplayname.md)
  
#### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

