---
title: "EncryptedSharedFolderDataCollection"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: "The EncryptedSharedFolderDataCollection element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients."
---

# EncryptedSharedFolderDataCollection

The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients. 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 **ArrayOfEncryptedSharedFolderDataType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[EncryptedSharedFolderData](encryptedsharedfolderdata.md) <br/> |Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
   
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

- [GetSharingMetadata operation](getsharingmetadata-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

