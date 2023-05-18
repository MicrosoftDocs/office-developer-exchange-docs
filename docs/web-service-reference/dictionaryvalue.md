---
title: "DictionaryValue"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DictionaryValue
api_type:
- schema
ms.assetid: f4089381-826f-4f6a-8c6d-e51b910cbe6d
description: "The DictionaryValue element specifies the dictionary value for a dictionary property."
---

# DictionaryValue

The **DictionaryValue** element specifies the dictionary value for a dictionary property. 
  
```xml
<DictionaryValue>
   <Type/>
   <Value/>
</DictionaryValue>
```

 **UserConfigurationDictionaryObjectType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Type (UserConfiguration)](type-userconfiguration.md) <br/> |Specifies the dictionary object type.  <br/> |
|[Value (UserConfiguration)](value-userconfiguration.md) <br/> |Specifies the dictionary object value as a string.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Specifies the contents of a single dictionary entry property.  <br/> |
   
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

