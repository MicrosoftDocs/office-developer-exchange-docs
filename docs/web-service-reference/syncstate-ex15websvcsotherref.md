---
title: "SyncState"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: "The SyncState element contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state."
---

# SyncState

The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state. 
  
```xml
<SyncState/>
```

 **String**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Defines a request to synchronize a folder hierarchy on a client.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a SyncFolderHierarchy request.  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Defines a request to synchronize items in an Exchange store folder.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contains the status and result of a SyncFolderItems request.  <br/> |
   
## Text value

A text value is required when this element is used.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SyncFolderItems operation](syncfolderitems-operation.md)
  
[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

