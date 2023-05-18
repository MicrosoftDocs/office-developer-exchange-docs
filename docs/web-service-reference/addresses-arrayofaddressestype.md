---
title: "Addresses (ArrayOfAddressesType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: "The Addresses element specifies an array of Address elements."
---

# Addresses (ArrayOfAddressesType)

The **Addresses** element specifies an array of **Address** elements. 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 **ArrayOfAddressesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Address (ContactType)](address-contacttype.md) <br/> |Specifies the address of a contact.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Contact (ContactType)](contact-contacttype.md) <br/> |Specifies a contact in the Unified Contact Store.  <br/> |
   
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

