---
title: "SetItemField"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: "The SetItemField element represents an update to a single property of an item in an UpdateItem operation."
---

# SetItemField

The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).
  
```
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

 **SetItemFieldType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies extended MAPI properties to set.  <br/> |
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message to update.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item to update.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item to update.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list to update.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message to update.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request to update.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response to update.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation to update.  <br/> |
|[Task](task.md) <br/> |Represents a task to update.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Updates (Item)](updates-item.md) <br/> |Contains a set of elements that define append, set, and delete changes to item properties.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[UpdateItem operation](updateitem-operation.md)

