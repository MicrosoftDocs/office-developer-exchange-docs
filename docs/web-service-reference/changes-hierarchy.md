---
title: "Changes (Hierarchy)"
 
 
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
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: "The Changes element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007."
---

# Changes (Hierarchy)

The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Changes (Hierarchy)](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 **SyncFolderHierarchyChangesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifies a single folder to create in the local client store.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifies a single folder to update in the local client store.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifies a single folder to delete in the local client store.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a SyncFolderHierarchy request.  <br/> |
   
## Text value

A text value that represents a Boolean value is required.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md)


[EWS reference for Exchange](ews-reference-for-exchange.md)
  
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

