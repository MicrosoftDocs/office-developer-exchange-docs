---
title: "DocumentSharingLocations (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 394f6015-721b-4800-9286-039d430f09b3
description: "The DocumentSharingLocations element contains a list of location and metadata information for a document sharing location."
---

# DocumentSharingLocations (SOAP)

The **DocumentSharingLocations** element contains a list of location and metadata information for a document sharing location. 
  
```XML
<DocumentSharingLocations>
   <DocumentSharingLocation />
</DocumentSharingLocations>
```

 **DocumentSharingLocations**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Contains the location and metadata for a document sharing location.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md) <br/> |Represents a user setting that is a collection of documentation sharing locations and metadata.  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
- [Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

