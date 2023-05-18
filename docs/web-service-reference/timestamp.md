---
title: "TimeStamp"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: "The Timestamp element represents the timestamp of a mailbox event."
---

# TimeStamp

The **Timestamp** element represents the timestamp of a mailbox event. 
  
```xml
<TimeStamp/>
```

 **DateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Represents an event where an item or folder is copied.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Represents an event where an item or folder is created.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Represents an event where an item or folder is deleted.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Represents an event where an item or folder is modified.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event where an item or folder is moved from one parent folder to another parent folder.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Represents an event triggered by a new mail item in a mailbox.  <br/> |
   
## Text value

This property is read-only.
  
## Remarks

This element is primarily available for use in client determination of event frequency. This is not present in [StatusEvent](statusevent.md).
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)

