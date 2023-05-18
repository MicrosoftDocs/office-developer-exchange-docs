---
title: "CreatedEvent"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreatedEvent
api_type:
- schema
ms.assetid: f0e53a53-c352-42a5-8280-cd808b0e961b
description: "The CreatedEvent element represents an event in which an item or folder is created."
---

# CreatedEvent

The **CreatedEvent** element represents an event in which an item or folder is created. 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</CreatedEvent>
```

**BaseObjectChangedEventType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Represents an event bookmark in the mailbox events table.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Represents the timestamp of a created item or folder mailbox event.  <br/> |
|[FolderId](folderid.md) <br/> |Represents the identifier of the created folder.  <br/> |
|[ItemId](itemid.md) <br/> |Represents the identifier of the created item.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder of the created item or folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

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
- [Using Pull Subscriptions](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [Event notifications in EWS](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

