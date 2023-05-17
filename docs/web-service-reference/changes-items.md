---
title: "Changes (Items)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Changes
api_type:
- schema
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: "The Changes element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server."
---

# Changes (Items)

The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Changes (Items)](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
   <ReadFlagChange/>
</Changes>
```

 **SyncFolderItemsChangesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifies a single item to create in the local client store.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifies a single item to update in the local client store.  <br/> |
|[Delete (ItemSync)](delete-itemsync.md) <br/> |Identifies a single item to delete in the local client store.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read. This property is read-only.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SyncFolderItems operation](syncfolderitems-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

