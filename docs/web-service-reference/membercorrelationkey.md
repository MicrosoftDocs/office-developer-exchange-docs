---
title: "MemberCorrelationKey"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 60cc7094-2e31-49d2-8598-181bcfb5f130
description: "The MemberCorrelationKey element specifies the identifiers of the contacts that are part of the instant messaging (IM) group."
---

# MemberCorrelationKey

The **MemberCorrelationKey** element specifies the identifiers of the contacts that are part of the instant messaging (IM) group. 
  
```XML
<MemberCorrelationKey>
   <ItemId/>
</MemberCorrelationKey>
```

**NonEmptyArrayOfItemIdsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ItemId](itemid.md)
  
### Parent elements

[ImGroup](imgroup.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

