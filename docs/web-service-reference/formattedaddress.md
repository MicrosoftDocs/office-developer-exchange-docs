---
title: "FormattedAddress"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 643f8663-1fab-4625-a7e9-5724e352972b
description: "The FormattedAddress element specifies the formatted display value of the associated postal address."
---

# FormattedAddress

The **FormattedAddress** element specifies the formatted display value of the associated postal address. 
  
```XML
<FormattedAddress></FormattedAddress>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) <br/> |Specifies information associated with a postal address.  <br/> |
|[PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md) <br/> |Specifies the postal address of the location.  <br/> |
   
## Text value

The text value of the **FormattedAddress** element is a string value that specifies the formatted address. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

