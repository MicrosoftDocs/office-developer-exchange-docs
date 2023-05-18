---
title: "Language (DiscoverySearchConfigurationType)"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: "The Language (DiscoverySearchConfigurationType) element identifies the culture to be used for the culture-specific format of date ranges. It also specifies the language used in a search query."
---

# Language (DiscoverySearchConfigurationType)

The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges. It also specifies the language used in a search query. 
  
```XML
<Language />
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## Text value

The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language. 
  
## Remarks

This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).
  
This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

