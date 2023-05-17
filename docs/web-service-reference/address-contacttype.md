---
title: "Address (ContactType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c39f37bf-5cf5-47a7-8a2a-337b5e68f94f
description: "The Address element specifies the address of a contact."
---

# Address (ContactType)

The **Address** element specifies the address of a contact. 
  
```XML
<Address></Address>
```

 **xs:string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Addresses (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Specifies an array of **Address** elements.  <br/> |
   
## Text value

The text value of the **Address** element is the contact's postal address. 
  
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

