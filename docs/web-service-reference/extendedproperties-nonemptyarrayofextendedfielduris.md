---
title: "ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 282ddb7f-00e3-4260-ab85-73fea9317c0e
description: "The ExtendedProperties element contains the extended properties used for the Unified Contact Store operations."
---

# ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)

The **ExtendedProperties** element contains the extended properties used for the Unified Contact Store operations. 
  
```XML
<ExtendedProperties>
   <ExtendedProperty/>
</ExtendedProperties>
```

 **NonEmptyArrayOfExtendedFieldURIs**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ExtendedProperty (PathToExtendedFieldType)](extendedproperty-pathtoextendedfieldtype.md)
  
### Parent elements

[GetImItems](getimitems.md) | [GetImItemList](getimitemlist.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

