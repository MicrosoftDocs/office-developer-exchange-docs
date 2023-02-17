---
title: "DocumentSharingLocation (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: "The DocumentSharingLocation element contains location and metadata information for a document sharing location."
---

# DocumentSharingLocation (SOAP)

The **DocumentSharingLocation** element contains location and metadata information for a document sharing location. 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 **DocumentSharingLocation**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Represents the URL of the document sharing web service.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Represents the URL of the document sharing location.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Represents the name of the document sharing location to use in the UI.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Represents the file extensions that can be stored in the document sharing location.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Indicates whether the document sharing location is available to outside connections.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Indicates whether access to the sharing location requires an authenticated user.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Indicates whether the user can modify access permissions to the document sharing location.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Indicates whether the document sharing location is the user's default sharing location.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Contains a list of document sharing locations and metadata.  <br/> |
   
## Text value

None.
  
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

