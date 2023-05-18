---
title: "GetDiscoverySearchConfiguration"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: "The GetDiscoverySearchConfiguration element specifies a request to retrieve the eDiscovery search configuration."
---

# GetDiscoverySearchConfiguration

The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration. 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 **GetDiscoverySearchConfigurationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |Specifies the identifier of the search.  <br/> |
|[ExpandGroupMembership](expandgroupmembership.md) <br/> |Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.  <br/> |
   
### Parent elements

None.
  
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

