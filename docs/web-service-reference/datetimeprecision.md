---
title: "DateTimePrecision"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: "The DateTimePrecision element specifies the precision for returned date/time values."
---

# DateTimePrecision

The **DateTimePrecision** element specifies the precision for returned date/time values. 
  
```XML
<DateTimePrecision />
```

**DateTimePrecisionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

None.
  
### Parent elements

The **DateTimePrecision** element is located in the SOAP header. 
  
## Text value

A text value is required. The following are the possible values:
  
- Seconds
    
- Milliseconds
    
## Remarks

When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00). When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000). 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

