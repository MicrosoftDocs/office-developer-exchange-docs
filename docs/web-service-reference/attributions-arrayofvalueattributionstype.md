---
title: "Attributions (ArrayOfValueAttributionsType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: "The Attributions element specifies an array of attributions for its associated Value element."
---

# Attributions (ArrayOfValueAttributionsType)

The **Attributions** element specifies an array of attributions for its associated **Value** element. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Attribution (string)](attribution-string.md) <br/> |Specifies a string used to identify an attribute.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Specifies the body content of an item.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Specifies an instance of an array of email addresses and their associated attributions.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Specifies extended properties for a persona.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Specifies an instance of an array of phone numbers and their associated attributions.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Specifies an instance of an array of postal addresses and their associated attributions.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Specifies an instance of an array of string data for a persona element.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Specifies an instance in an array of attributes associated with a persona element.  <br/> |
   
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

