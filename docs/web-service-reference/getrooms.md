---
title: "GetRooms"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 82a737c7-da41-4777-8ad8-89851a0b602b
description: "The GetRooms element is the root element in a request to get a list of rooms within a particular room list."
---

# GetRooms

The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list. 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 **GetRoomsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[RoomList](roomlist.md) <br/> |Represents an e-mail address that identifies a list of meeting rooms  <br/> |
   
#### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

