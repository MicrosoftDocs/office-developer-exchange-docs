---
title: "Offset"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: "The Offset element describes the offset from the BaseOffset. Together with the BaseOffset element, the Offset element identifies whether the time is standard or daylight saving time."
---

# Offset

The **Offset** element describes the offset from the [BaseOffset](baseoffset.md). Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time. 
  
```xml
<Offset/>
```

 **duration**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Daylight](daylight.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
|[Standard](standard.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
   
## Text value

The text value represents the offset from Coordinated Universal Time (UTC).
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

