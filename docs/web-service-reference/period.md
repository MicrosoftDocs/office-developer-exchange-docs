---
title: "Period"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: "The Period element defines the name, time offset, and unique identifier for a specific stage of the time zone."
---

# Period

The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone. 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 **PeriodType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Bias  <br/> |An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.  <br/> |
|Name  <br/> |A string value that represents the descriptive name of the period.  <br/> |
|Id  <br/> |A string value that represents the identifier for the period.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Periods](periods.md) <br/> |Represents an array of periods that define the time offset at different stages of the time zone.  <br/> |
   
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

