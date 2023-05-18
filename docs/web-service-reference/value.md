---
title: "Value"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: "The Value element contains the value of an extended property."
---

# Value

The **Value** element contains the value of an extended property. 
  
```xml
<Value/>
```

**String**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Values](values.md) <br/> |Contains a collection of values for an extended property.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
   
## Text value

The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.
  
## Remarks

A **Value** element can occur in both single and multivalued extended property instances. For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element. For multivalued instance, it exists as a direct child of the **Values** collection. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

