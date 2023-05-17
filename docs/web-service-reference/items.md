---
title: "Items"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: "The Items element contains an array of items."
---

# Items

The **Items** element contains an array of items. 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 **ArrayOfRealItemsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contains the status and result of a [CopyItem operation](copyitem-operation.md) request.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contains the status and result of a [GetItem operation](getitem-operation.md) request.  <br/> |
|[GroupedItems](groupeditems.md) <br/> |Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contains the status and result of a [MoveItem operation](moveitem-operation.md) request.  <br/> |
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contains the status and result of an [UpdateItem operation](updateitem-operation.md) request.  <br/> |
   
## Remarks

For information about the set of items in a [CreateItem operation](createitem-operation.md) request, see [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).
  
[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema. Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements. Versions of Exchange starting with Exchange Server 2010 do not return the base [Item](item.md) element in responses. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[EWS reference for Exchange](ews-reference-for-exchange.md)
  
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

