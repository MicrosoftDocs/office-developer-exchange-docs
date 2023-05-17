---
title: "Rooms"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: "The Rooms element is a list of one or more elements that represent meeting rooms."
---

# Rooms

The **Rooms** element is a list of one or more elements that represent meeting rooms. 
  
[GetRoomsResponse](getroomsresponse.md)
  
[Rooms](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 **ArrayOfRoomsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Room](room.md) <br/> |Defines an e-mail address and display name that represents a meeting room.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetRoomsResponse](getroomsresponse.md) <br/> ||
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetRooms operation](getrooms-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

