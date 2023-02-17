---
title: "AnonymousAccessAllowed (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: "The AnonymousAccessAllowed element indicates whether a document sharing location requires an authenticated user."
---

# AnonymousAccessAllowed (SOAP)

The **AnonymousAccessAllowed** element indicates whether a document sharing location requires an authenticated user. 
  
```XML
<AnonymousAccessAllowed /> 
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

The Boolean value of the **AnonymousAccessAllowed** element indicates whether the sharing location requires an authenticated user. 
  
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

