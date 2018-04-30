---
title: "DictionaryKey"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- DictionaryKey
api_type:
- schema
ms.assetid: f331c8ac-f1c7-4248-a570-97701969d5bf
description: "The DictionaryKey element specifies the dictionary key for a dictionary property."
---

# DictionaryKey

The **DictionaryKey** element specifies the dictionary key for a dictionary property. 
  
```
<DictionaryKey>
   <Type/>
   <Value/>
</DictionaryKey>
```

 **UserConfigurationDictionaryObjectType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Type (UserConfiguration)](type-userconfiguration.md) <br/> | Specifies a dictionary object type. The type can be one of the following string values:  <br/>  DateTime  <br/>  Boolean  <br/>  Byte  <br/>  String  <br/>  Integer32  <br/>  UnsignedInteger32  <br/>  Integer64  <br/>  UnsignedInteger64  <br/>  StringArray  <br/>  ByteArray  <br/> |
|[Value (UserConfiguration)](value-userconfiguration.md) <br/> |Specifies the dictionary object value as a string.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Specifies the contents of a single dictionary entry property.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

