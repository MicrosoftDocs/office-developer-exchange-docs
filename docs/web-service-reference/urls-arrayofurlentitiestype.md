---
title: "Urls (ArrayOfUrlEntitiesType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c39744ea-0cee-4954-8653-8279d6b10161
description: "The Urls element specifies an array of URLs that are the result of entity extraction from an item in the mailbox."
---

# Urls (ArrayOfUrlEntitiesType)

The **Urls** element specifies an array of URLs that are the result of entity extraction from an item in the mailbox. 
  
```XML
<Urls>
   <UrlEntity/>
</Urls>
```

 **ArrayOfUrlEntitiesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[UrlEntity](urlentity.md)
  
### Parent elements

[EntityExtractionResult](entityextractionresult.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   