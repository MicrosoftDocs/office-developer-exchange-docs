---
title: "RoomLists"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: "The RoomLists element is a list of one or more addresses that represent a list of meeting rooms."
---

# RoomLists

The **RoomLists** element is a list of one or more addresses that represent a list of meeting rooms. 
  
[GetRoomListsResponse](getroomlistsresponse.md)
  
[RoomLists](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 **ArrayOfEmailAddressesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Address (EmailAddressType)](address-emailaddresstype.md) <br/> |Defines the e-mail address and display name that represents the room list. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |Contains the status and result of a [GetRoomLists operation](getroomlists-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetRoomLists operation](getroomlists-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

