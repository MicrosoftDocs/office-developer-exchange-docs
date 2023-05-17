---
title: "DiscoverySearchConfigurations"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f04b14c9-384c-4016-b113-52a49e15e73b
description: "The DiscoverySearchConfigurations element specifies an array of DiscoverySearchConfiguration elements."
---

# DiscoverySearchConfigurations

The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements. 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 **ArrayOfDiscoverySearchConfigurationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DiscoverySearchConfiguration](discoverysearchconfiguration.md) <br/> |Specifies the configuration for eDiscovery search.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDiscoverySearchConfigurationResponseMessage](getdiscoverysearchconfigurationresponsemessage.md) <br/> |Specifies the response message for a **GetDiscoverySearchConfiguration** request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

