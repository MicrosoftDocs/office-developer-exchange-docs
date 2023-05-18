---
title: "DictionaryEntry"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DictionaryEntry
api_type:
- schema
ms.assetid: 531ea96a-d411-43e6-9fec-11fa2c959a30
description: "The DictionaryEntry element specifies the contents of a single dictionary entry property."
---

# DictionaryEntry

The **DictionaryEntry** element specifies the contents of a single dictionary entry property. 
  
```xml
<DictionaryEntry>
   <DictionaryKey/>
   <DictionaryValue/>
</DictionaryEntry>
```

 **UserConfigurationDictionaryEntryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DictionaryKey](dictionarykey.md) <br/> |Specifies the dictionary key for a dictionary property.  <br/> |
|[DictionaryValue](dictionaryvalue.md) <br/> |Specifies the dictionary value for a dictionary property.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Dictionary](dictionary.md) <br/> |Defines a set of dictionary property entries for a user configuration object.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

