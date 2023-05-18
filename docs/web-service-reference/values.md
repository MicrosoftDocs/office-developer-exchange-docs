---
title: "Values"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Values
api_type:
- schema
ms.assetid: 4b14c714-51fa-4225-82ad-83ba9f611824
description: "The Values element contains a collection of values for an extended property."
---

# Values

The **Values** element contains a collection of values for an extended property. 
  
```xml
<Values>
   <Value/>
</Values>
```

**NonEmptyArrayOfPropertyValuesType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Value](value.md) <br/> |Contains a value of an extended property.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

