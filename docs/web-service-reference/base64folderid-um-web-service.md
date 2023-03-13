---
title: "base64FolderId (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: "The base64FolderId element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a SetTelephoneAccessFolderEmail operation (UM web service) request."
---

# base64FolderId (UM web service)

The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request. 
  
[SetTelephoneAccessFolderEmail (UM web service)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (UM web service)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (UM web service)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Defines request to set the telephone access e-mail folder.  <br/> |
   
## Text value

A text value is required. The text value represents the MAPI ID of the folder.
  
## Remarks

To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SetTelephoneAccessFolderEmail (UM web service)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder operation](findfolder-operation.md)
  
[FindItem operation](finditem-operation.md)

