---
title: "Dictionary"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Dictionary
api_type:
- schema
ms.assetid: 8309e468-115b-4d6e-b33c-c4719dcecc4c
description: "The Dictionary element defines a set of dictionary property entries for a user configuration object."
---

# Dictionary

The **Dictionary** element defines a set of dictionary property entries for a user configuration object. 
  
```xml
<Dictionary>
   <DictionaryEntry/>
</Dictionary>
```

 **UserConfigurationDictionaryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Specifies the contents of a single dictionary entry property.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserConfiguration](userconfiguration.md) <br/> |Defines a single user configuration object.  <br/> |
   
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

