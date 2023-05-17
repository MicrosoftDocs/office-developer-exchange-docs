---
title: "HomeAddresses"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 57fb1b9d-2ba8-4359-ae79-35c0d56a2d0f
description: "The HomeAddresses element specifies an array of home addresses and the identifiers of their source attributions for the associated persona."
---

# HomeAddresses

The **HomeAddresses** element specifies an array of home addresses and the identifiers of their source attributions for the associated persona. 
  
```XML
<HomeAddresses>
    <PostalAddressAttributedValue/>
</HomeAddresses>
```

 **ArrayOfPostalAddressAttributedValuesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Specifies an instance of an array of postal addresses and their associated attributions.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Specifies a set of persona data returned by a **GetPersona** request.  <br/> |
   
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

