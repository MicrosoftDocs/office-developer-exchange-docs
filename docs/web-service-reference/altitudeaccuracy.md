---
title: "AltitudeAccuracy"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: aadc1f90-e9ab-4411-b51f-2d43e5e22f2a
description: "The AltitudeAccuracy element specifies the accuracy of the altitude property for a postal address."
---

# AltitudeAccuracy

The **AltitudeAccuracy** element specifies the accuracy of the altitude property for a postal address. 
  
```XML
<AltitudeAccuracy></AltitudeAccuracy>
```

 **xs:double**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md) <br/> |Specifies the postal address of the location.  <br/> |
   
## Text value

The text value of the **AltitudeAccuracy** element is the accuracy estimate for the altitude property of a postal address. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

