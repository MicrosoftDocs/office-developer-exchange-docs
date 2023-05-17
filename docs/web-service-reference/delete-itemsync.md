---
title: "Delete (ItemSync)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- schema
ms.assetid: 4f372d57-2e39-46af-9d83-6c8c55108587
description: "The Delete element identifies a single item to delete in the local client store."
---

# Delete (ItemSync)

The **Delete** element identifies a single item to delete in the local client store. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md)  
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)  
- [Changes (Items)](changes-items.md)  
- [Delete (ItemSync)](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

**SyncFolderItemsDeleteType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.  <br/> |
   
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

