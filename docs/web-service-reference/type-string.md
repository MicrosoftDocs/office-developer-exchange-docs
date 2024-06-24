---
title: "Type (string)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d5eea7a8-c40d-42a6-8e0d-67f3252496cf
description: "The Type element specifies the type of postal address or phone number, for example,HomeorBusiness."
---

# Type (string)

The **Type** element specifies the type of postal address or phone number, for example, "Home" or "Business". 
  
```XML
<Type></Type>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Phone](phone.md) | [PhoneNumber](phonenumber.md) | [Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## Text value

The text value of the **Type** element is the type of a postal address or phone number. For example, the values "Home" or "Business" are expected values for the **Type** element. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

