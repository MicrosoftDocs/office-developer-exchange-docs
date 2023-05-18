---
title: "SyncFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncFolderId
api_type:
- schema
ms.assetid: 3645fa03-236d-4e5f-b8b9-5d98f7f35fa2
description: "The SyncFolderId element represents the folder that contains the items to synchronize."
---

# SyncFolderId

The **SyncFolderId** element represents the folder that contains the items to synchronize. 
  
```xml
<SyncFolderId>
   <FolderId/>
</SyncFolderId>
```

```xml
<SyncFolderId>
   <DistinguishedFolderId/> 
</SyncFolderId>
```

**TargetFolderIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Defines a request to synchronize a folder hierarchy in an Exchange store.  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Defines a request to synchronize items in an Exchange store folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [SyncFolderItems operation](syncfolderitems-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
