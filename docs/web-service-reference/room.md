---
title: "Room"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: "The Room element represents a meeting room."
---

# Room

The **Room** element represents a meeting room. 
  
[Rooms](rooms.md)
  
[Room](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 **RoomType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Id (EmailAddressType)](id-emailaddresstype.md) <br/> |An identifier that contains an email address and display name that represents the meeting room.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rooms](rooms.md) <br/> |Defines a list of meeting rooms associated with a common feature, such as being located in the same building.  <br/> |
   
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

- [GetRooms operation](getrooms-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
