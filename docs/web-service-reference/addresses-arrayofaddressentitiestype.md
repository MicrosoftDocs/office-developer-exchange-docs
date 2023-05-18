---
title: "Addresses (ArrayOfAddressEntitiesType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e
description: "The Addresses element specifies an array of AddressEntity elements."
---

# Addresses (ArrayOfAddressEntitiesType)

The **Addresses** element specifies an array of **AddressEntity** elements. 
  
```XML
<Addresses>
   <AddressEntity/>
</Addresses>
```

 **ArrayOfAddressEntitiesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AddressEntity](addressentity.md) <br/> |Specifies a single address entity.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |Specifies the **EntityExtractionResult** property of an item.  <br/> |
   
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

