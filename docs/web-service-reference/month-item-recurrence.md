---
title: "Month (Item Recurrence)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Month
api_type:
- schema
ms.assetid: d2352001-f959-436a-afd5-a0a07b8ae02a
description: "The Month element describes the month when a yearly recurring item occurs."
---

# Month (Item Recurrence)

The **Month** element describes the month when a yearly recurring item occurs. 
  
```xml
<Month/>
```

 **MonthNamesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Represents a yearly recurrence pattern.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describes a relative yearly recurrence pattern.  <br/> |
   
## Text value

A text value is required. The following are the possible text values for this element:
  
- January
    
- February
    
- March
    
- April
    
- May
    
- June
    
- July
    
- August
    
- September
    
- October
    
- November
    
- December
    
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

