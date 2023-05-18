---
title: "CopiedEvent"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: "The CopiedEvent element represents an event in which an item or folder is copied."
---

# CopiedEvent

The **CopiedEvent** element represents an event in which an item or folder is copied. 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</CopiedEvent>
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
|[TimeStamp](timestamp.md) <br/> |Represents the timestamp of a copy item/folder mailbox event.  <br/> |
|[FolderId](folderid.md) <br/> |Represents the identifier of the folder.  <br/> |
|[ItemId](itemid.md) <br/> |Represents the identifier of the item.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the folder that contains the copy.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Represents the folder identifier of the original folder before it was copied.  <br/> |
|[OldItemId](olditemid.md) <br/> |Contains the unique identifier of the original item before it was copied.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Contains the identifier of the original parent folder of an item or folder that was copied.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [Subscribe operation](subscribe-operation.md) 
- [GetEvents operation](getevents-operation.md) 
- [Unsubscribe operation](unsubscribe-operation.md)
- [Using Pull Subscriptions](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [Push Notification Sample Application](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

