---
title: "SharingFolderId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: "The SharingFolderId element represents the identifier of the local folder in a sharing relationship."
---

# SharingFolderId

The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship. 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Contains a string that identifies a folder in the Exchange store. This attribute is required.  <br/> |
|ChangeKey  <br/> |Contains a string that identifies a version of a folder that is identified by the Id attribute. This attribute is optional. Use this attribute to make sure that the correct version of a folder is used.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RefreshSharingFolder](refreshsharingfolder.md) <br/> |Defines a request to refresh the specified local folder.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

