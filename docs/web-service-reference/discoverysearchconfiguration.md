---
title: "DiscoverySearchConfiguration"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: "The DiscoverySearchConfiguration element specifies the configuration for eDiscovery search."
---

# DiscoverySearchConfiguration

The **DiscoverySearchConfiguration** element specifies the configuration for eDiscovery search. 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 **DiscoverySearchConfigurationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |Specifies the identifier of the search.  <br/> |
|[SearchQuery](searchquery.md) <br/> |Specifies the name of an eDiscovery search query.  <br/> |
|[SearchableMailboxes](searchablemailboxes.md) <br/> |Contains a list of the mailboxes returned from a **GetSearchableMailboxes** request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DiscoverySearchConfigurations](discoverysearchconfigurations.md) <br/> |Specifies an array of **DiscoverySearchConfiguration** elements.  <br/> |
   
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

