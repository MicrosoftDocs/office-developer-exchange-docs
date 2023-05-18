---
title: "Constant"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: "The Constant element identifies a constant value in a restriction."
---

# Constant

The **Constant** element identifies a constant value in a restriction. 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Value** <br/> |Specifies the value to compare in the restriction.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Contains](contains.md) <br/> |Represents a search expression that determines whether a given property contains the supplied constant string value.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Represents either a property or a constant value to be used when comparing with another property.  <br/> |
   
## Remarks

The string value in the **Value** attribute must be coercible into the type you are trying to compare against. For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

