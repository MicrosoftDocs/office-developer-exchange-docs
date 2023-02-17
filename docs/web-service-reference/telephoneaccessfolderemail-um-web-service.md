---
title: "TelephoneAccessFolderEmail (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- TelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 5d32ae22-bb9f-4352-a251-d516b66ff35b
description: "The TelephoneAccessFolderEmail element contains a value that species the identifier of the e-mail folder from which Unified Messaging will read messages over a telephone as contained in a response to a GetUMProperties operation (UM web service) request."
 
 
---

# TelephoneAccessFolderEmail (UM web service)

The **TelephoneAccessFolderEmail** element contains a value that species the identifier of the e-mail folder from which Unified Messaging will read messages over a telephone as contained in a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request. 
  
[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md)
  
[TelephoneAccessFolderEmail (UM web service)](telephoneaccessfolderemail-um-web-service.md)
  
```xml
<TelephoneAccessFolderEmail/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md) <br/> |Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.  <br/> |
   
## Text value

A text value is required.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md)
  
- [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md)