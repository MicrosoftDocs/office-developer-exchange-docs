---
title: "CanModifyPermissions (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: "The CanModifyPermissions element indicates whether a user can modify access permissions to a document sharing location."
 
 
---

# CanModifyPermissions (SOAP)

The **CanModifyPermissions** element indicates whether a user can modify access permissions to a document sharing location. 
  
```XML
<CanModifyPermissions /> 
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Represents location and metadata information for a document sharing location.  <br/> |
   
## Text value

The Boolean value of the **CanModifyPermissions** element indicates whether users can modify access permissions to the sharing location. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)


[Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

