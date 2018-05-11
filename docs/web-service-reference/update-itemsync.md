---
title: "Update (ItemSync)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: "The Update element identifies a single item to update in the local client store."
---

# Update (ItemSync)

The **Update** element identifies a single item to update in the local client store. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Changes (Items)](changes-items.md)
  
[Update (ItemSync)](update-itemsync.md)
  
```
<Update>
   <Item/>
</Update>
```

 **SyncFolderItemsCreateOrUpdateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Item](item.md) <br/> |Represents a generic Exchange item to update.  <br/> |
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
|[Changes (Items)](changes-items.md) <br/> |Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[SyncFolderItems operation](syncfolderitems-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

