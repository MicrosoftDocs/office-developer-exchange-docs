---
title: "RemoveItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: "The RemoveItem element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received."
---

# RemoveItem

The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received. 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 **RemoveItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ObjectName** <br/> |Represents the name of the RemoveItem reply object class as an English string.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Identifies the item to which the RemoveItem response object refers.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contains a collection of all the response objects that are associated with an item in the Exchange store.  <br/> |
   
## Remarks

 **RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md). Otherwise, an error is thrown.
  
> [!NOTE]
> The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled. 
  
To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.
  
 **RemoveItem** is not supported for delegate access. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

