---
title: "Create (ItemSync)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: "The Create element identifies a single item to create in the local client store."
---

# Create (ItemSync)

The **Create** element identifies a single item to create in the local client store. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) 
- [Changes (Items)](changes-items.md) 
- [Create (ItemSync)](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

**SyncFolderItemsCreateOrUpdateType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Item](item.md) <br/> |Represents a generic Exchange item to create.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message to create.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item to create.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item to create.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list to create.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting message to create.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request to create.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response to create.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation to create.  <br/> |
|[Task](task.md) <br/> |Represents a task to create.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.  <br/> |
   
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

- [SyncFolderItems operation](syncfolderitems-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

