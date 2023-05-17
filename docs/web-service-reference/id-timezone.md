---
title: "Id (TimeZone)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Id
api_type:
- schema
ms.assetid: 4c7350b4-ffa1-4e7d-9433-80b4383bd0d2
description: "The Id element identifies a single time zone definition."
---

# Id (TimeZone)

The **Id** element identifies a single time zone definition. 
  
```xml
<Id>...</Id>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Ids](ids.md) <br/> |Contains an array of time zone definition identifiers.  <br/> |
   
## Text value

A text value is required. The text value represents the unique identifier for time zone definition.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

