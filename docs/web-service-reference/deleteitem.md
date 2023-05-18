---
title: "DeleteItem"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: "The DeleteItem element defines a request to delete an item from a mailbox in the Exchange store."
---

# DeleteItem

The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store. 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**DeleteType** <br/> |Describes how an item is deleted. This attribute is required.  <br/> |
|**SendMeetingCancellations** <br/> |Describes whether a calendar item deletion is communicated to attendees. This attribute is required when calendar items are deleted. This attribute is optional if non-calendar items are deleted.  <br/> |
|**AffectedTaskOccurrences** <br/> |Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md). This attribute is required when tasks are deleted. This attribute is optional when non-task items are deleted.  <br/> |
|**SuppressReadReceipts** <br/> |Indicates whether read receipts for the deleted item are suppressed. A text value of **true**, indicates that the read receipts are suppressed. A value of **false** indicates that the read receipts are sent to the sender. This attribute is optional.  <br/> |
   
#### DeleteType attribute

|**Value**|**Description**|
|:-----|:-----|
|HardDelete  <br/> |An item is permanently removed from the store.  <br/> |
|SoftDelete  <br/> |An item is moved to the dumpster if the dumpster is enabled.  <br/> |
|MoveToDeletedItems  <br/> |An item is moved to the Deleted Items folder.  <br/> |
   
#### SendMeetingCancellations attribute

|**Value**|**Description**|
|:-----|:-----|
|SendToNone  <br/> |A calendar item is deleted without sending a cancellation message.  <br/> |
|SendOnlyToAll  <br/> |A calendar item is deleted and a cancellation message is sent to all attendees.  <br/> |
|SendToAllAndSaveCopy  <br/> |A calendar item is deleted and a cancellation message is sent to all attendees. A copy of the cancellation message is saved in the Sent Items folder.  <br/> |
   
#### AffectedTaskOccurrences attribute

|**Value**|**Description**|
|:-----|:-----|
|AllOccurrences  <br/> |A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |A delete item request deletes only specific occurrences of a task.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store. The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.  <br/> |
   
### Parent elements

None.
  
## Remarks

The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database. This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010. 
  
The **SoftDelete** option works differently for different target versions of Exchange. **SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future. **SoftDelete** for Exchange 2010 immediately moves the item to the dumpster. **SoftDelete** is not an option for folder deletion. **SoftDelete** traversal searches for items and folders will not return any results. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteItemResponse](deleteitemresponse.md)  
- [DeleteItem operation](deleteitem-operation.md)

