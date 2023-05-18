---
title: "SyncFolderHierarchy"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: "The SyncFolderHierarchy element defines a request to synchronize a folder hierarchy on a client."
---

# SyncFolderHierarchy

The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client. 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 **SyncFolderHierarchyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Represents the folder that contains the items to synchronize. This element is optional.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state.  <br/> |
   
### Parent elements

None.
  
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



[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

