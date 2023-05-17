---
title: "AbsoluteDate"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AbsoluteDate
api_type:
- schema
ms.assetid: 8bc59a26-6fe1-42e9-968c-69a94a3fb0ae
description: "The AbsoluteDate element represents the date when the time changes from standard or daylight saving time."
---

# AbsoluteDate

The **AbsoluteDate** element represents the date when the time changes from standard or daylight saving time. 
  
```xml
<AbsoluteDate/>
```

**date**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Standard](standard.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
|[Daylight](daylight.md) <br/> |Represents the date and time when the time changes from standard time to daylight saving time.  <br/> |
   
## Text value

The text value represents the date when the shift between standard or daylight saving time occurs.
  
## Remarks

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




