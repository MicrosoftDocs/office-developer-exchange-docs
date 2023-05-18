---
title: "Notifications"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: "The Notifications element contains an array of information about the subscription and the events that have occurred since the last notification."
---

# Notifications

The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification. 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 **NonEmptyArrayOfNotificationsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Messages schema; Types schema  <br/> |
|Validation File  <br/> |Messages.xsd; Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetFolder operation](getfolder-operation.md)

[DeleteFolder operation](deletefolder-operation.md)
  
[MoveFolder operation](movefolder-operation.md)
  
[CopyFolder operation](copyfolder-operation.md)
  
[Subscribe operation](subscribe-operation.md)

