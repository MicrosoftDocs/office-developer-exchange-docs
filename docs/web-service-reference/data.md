---
title: "Data"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Data
api_type:
- schema
ms.assetid: f875e6c2-be18-439a-a7b1-bb49a149b538
description: "The Data element contains encrypted data that represents the shared data."
---

# Data

The **Data** element contains encrypted data that represents the shared data. 
  
- [EncryptedSharedFolderData](encryptedsharedfolderdata.md)  
- [Data](data.md)
  
```xml
<Data/>
```

**EncryptedDataContainerType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EncryptedSharedFolderData](encryptedsharedfolderdata.md) <br/> |Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetSharingMetadata operation](getsharingmetadata-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)