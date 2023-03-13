---
title: "SetTelephoneAccessFolderEmail (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 90759da7-6dba-499e-b8c8-e44a016b3198
description: "The SetTelephoneAccessFolderEmail element defines a request to set the default e-mail folder from which Unified Messaging will read messages over the telephone."
 
 
---

# SetTelephoneAccessFolderEmail (UM web service)

The **SetTelephoneAccessFolderEmail** element defines a request to set the default e-mail folder from which Unified Messaging will read messages over the telephone. 
  
[SetTelephoneAccessFolderEmail (UM web service)](settelephoneaccessfolderemail-um-web-service.md)
  
```xml
<SetTelephoneAccessFolderEmail>
  <base64FolderId>   </base64FolderId>
</SetTelephoneAccessFolderEmail>
```

 **complexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[base64FolderId (UM web service)](base64folderid-um-web-service.md) <br/> |The identifier of the e-mail folder.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md)

