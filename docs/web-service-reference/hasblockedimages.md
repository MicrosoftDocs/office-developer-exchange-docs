---
title: "HasBlockedImages"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: "The HasBlockedImages element specifies a Boolean value that indicates whether the item has blocked images."
---

# HasBlockedImages

The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images. 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
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
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
   
## Text value

A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images. A value of **false** indicates that the item does not have any blocked images. 
  
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

