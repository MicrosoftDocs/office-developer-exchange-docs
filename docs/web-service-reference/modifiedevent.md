---
title: "ModifiedEvent"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: "The ModifiedEvent element represents an event in which an item or folder is modified."
---

# ModifiedEvent

The **ModifiedEvent** element represents an event in which an item or folder is modified. 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

**ModifiedEventType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Represents an event bookmark in the mailbox events table.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Represents the timestamp of a modified item or folder mailbox event.  <br/> |
|[FolderId](folderid.md) <br/> |Represents the identifier of the modified folder.  <br/> |
|[ItemId](itemid.md) <br/> |Represents the identifier of the modified item.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder of the modified item or folder.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Represents the count of unread items within a given folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

Two modified events are generated for each modification of an item in a folder. One event is relevant to the item that changed. The other event is relevant to the parent folder of the item. This is the same folder that the subscription was created against. The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [Subscribe operation](subscribe-operation.md)  
- [GetEvents operation](getevents-operation.md)  
- [Unsubscribe operation](unsubscribe-operation.md)

