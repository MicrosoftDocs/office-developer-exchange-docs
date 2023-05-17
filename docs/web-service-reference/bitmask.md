---
title: "Bitmask"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: "The Bitmask element represents a hexadecimal or decimal mask to be used during an Excludes restriction operation."
---

# Bitmask

The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation. 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Value** | Represents a decimal or hexadecimal bitmask. The value is represented by the following regular expression:<br/>`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.<br/><br/>The following are examples of hexadecimal values for this attribute:<br/>- 0x12AF<br/>- 0X334AE<br/><br/>The following are examples of decimal values for this attribute:<br/>- 10<br/>- 255<br/>- 4562 |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Excludes](excludes.md) <br/> |Performs a bitwise mask of the properties.  <br/> |
   
## Remarks

Hexadecimal values must have a prefix of either 0x or 0X. If this prefix does not exist, the value is assumed to be a decimal number.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

