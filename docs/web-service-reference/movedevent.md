---
title: "MovedEvent"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: "The MovedEvent element represents an event in which an item or folder is moved from one parent folder to another parent folder."
---

# MovedEvent

The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder. 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</MovedEvent>
```


**MovedCopiedEventType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Represents an events bookmark in the mailbox events table.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Represents the timestamp of a move item/folder mailbox event.  <br/> |
|[FolderId](folderid.md) <br/> |Represents the identifier of the moved folder.  <br/> |
|[ItemId](itemid.md) <br/> |Represents the identifier of the moved item.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the folder that contains the moved item or folder.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Contains the folder identifier of the original folder before it was moved or copied.  <br/> |
|[OldItemId](olditemid.md) <br/> |Contains the unique identifier of the original item before it was moved.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Contains the identifier of the original parent folder of an item or folder that was moved.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [Subscribe operation](subscribe-operation.md) 
- [GetEvents operation](getevents-operation.md) 
- [Unsubscribe operation](unsubscribe-operation.md)

