---
title: "CountryOrRegion"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CountryOrRegion
api_type:
- schema
ms.assetid: e978cd19-96ce-4ebf-81df-eadf2d775132
description: "The Country element represents the country or region for a given physical address."
---

# CountryOrRegion

The **Country** element represents the country or region for a given physical address. 
  
```xml
<Country/>
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
|[Entry (PhysicalAddress)](entry-physicaladdress.md) <br/> |Describes a single physical address for a contact item.  <br/> |
   
## Text value

The text value is a string value that represents the name of a country.
  
## Remarks

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

