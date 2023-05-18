---
title: "ClientExtension"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: "The ClientExtension element contains user and configuration information about an app."
---

# ClientExtension

The **ClientExtension** element contains user and configuration information about an app. 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 **ClientExtensionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|IsAvailable  <br/> |Specifies whether the app is available. A text value of **true** for the **IsAvailable** attribute indicates that the app is available. A value of **false** indicates that the app is not available. This attribute is optional.  <br/> |
|IsMandatory  <br/> |Specifies whether the app is mandatory. A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox. A value of **false** indicates that the app is not mandatory. This attribute is optional.  <br/> |
|IsEnabledByDefault  <br/> |Specifies whether the app is enabled by default. A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default. A value of **false** indicates that the app is not enabled by default. This attribute is optional.  <br/> |
|ProvidedTo  <br/> |Specifies to whom the app is provided. This attribute is optional.  <br/> |
|Type  <br/> |Specifies the type of the app.  <br/> |
|Scope  <br/> |Specifies the scope of the app.  <br/> |
|MarketplaceAssetId  <br/> |Specifies the marketplace asset identifier of the app.  <br/> |
|MarketplaceContentMarket  <br/> |Specifies the marketplace content that a user sees for details and reviews about an app.  <br/> |
|AppStatus  <br/> |Specifies the status code of a mail app in an unexpected state.  <br/> |
|Etoken  <br/> |Specifies the license token for paid or trial mail apps.  <br/> |
   
#### Type

|**Value**|**Description**|
|:-----|:-----|
|Default  <br/> |Indicates that the app is available by default.  <br/> |
|Private  <br/> |Indicates that the app is private.  <br/> |
|MarketPlace  <br/> |Indicates that the app is a marketplace app.  <br/> |
   
#### Scope

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the app has no scope.  <br/> |
|User  <br/> |Indicates that the app is per user.  <br/> |
|Organization  <br/> |Indicates that the app is for an organization.  <br/> |
|Default  <br/> |Indicates that the app is a default app.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Specifies the email accounts that can access the app.  <br/> |
|[Manifest](manifest.md) <br/> |Contains the base-64 encoded app manifest file.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Specifies an array of **ClientExtension** elements.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

