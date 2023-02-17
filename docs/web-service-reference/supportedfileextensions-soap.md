---
title: "SupportedFileExtensions (SOAP)"
description: "The SupportedFileExtensions element lists the file extensions that can be stored in a document sharing location."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53 
---

# SupportedFileExtensions (SOAP)

The **SupportedFileExtensions** element lists the file extensions that can be stored in a document sharing location. 
  
```XML
<SupportedFileExtensions /> 
```

**ArrayOfFileExtension**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FileExtension (SOAP)](fileextension-soap.md) <br/> |Represents a file extension.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Represents location and metadata information for a document sharing location.  <br/> |
   
## Element information

|Element info|Value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
[Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
