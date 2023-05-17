---
title: "SyncFolderItems"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: "The SyncFolderItems element defines a request to synchronize items in an Exchange store folder."
---

# SyncFolderItems

The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder. 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>
   <SyncScope/>
</SyncFolderItems>
```

> [!NOTE]
> SyncFolderItems operation is not supported for use against Office 365 Group mailboxes.

 **SyncFolderItemsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifies the item properties and content to include in a SyncFolderItems response. This element is required.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Represents the folder that contains the items to synchronize. This element is required.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state. This element is optional.  <br/> |
|[Ignore](ignore.md) <br/> |Identifies items to skip during synchronization. This element is optional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Describes the maximum number of changes that can be returned in a synchronization response. This element is required.  <br/> |
|[SyncScope](syncscope.md) <br/> |Specifies whether just items or items and folder associated information are returned in a synchronization response. This element is optional.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SyncFolderItems operation](syncfolderitems-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

