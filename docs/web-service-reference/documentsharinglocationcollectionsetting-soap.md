---
title: "DocumentSharingLocationCollectionSetting (SOAP)"
description: "DocumentSharingLocationCollectionSetting element represents a user setting that is a collection of documentation sharing locations and metadata."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 0e3346f9-7a55-4e87-b121-9b1ee7f227f4
---

# DocumentSharingLocationCollectionSetting (SOAP)

The **DocumentSharingLocationCollectionSetting** element represents a user setting that is a collection of documentation sharing locations and metadata. 
  
[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md)
  
```XML
<DocumentSharingLocationCollectionSetting>
    <DocumentSharingLocations />
</DocumentSharingLocationCollectionSetting>
```

**DocumentSharingLocationCollectionSetting**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Represents the location and metadata for a list of document sharing locations.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Represents a collection of user settings.  <br/> |
   
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
