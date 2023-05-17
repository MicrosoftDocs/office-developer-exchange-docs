---
title: "AttendeeLocation"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 1344a087-88ea-472a-bebf-9b45245592fb
description: "The AttendeeLocation element specifies the location of an attendee for a calendar item."
---

# AttendeeLocation

The **AttendeeLocation** element specifies the location of an attendee for a calendar item. 
  
```XML
<AttendeeLocation></AttendeeLocation>
```

 **xs:string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[LocationBasedStateDefinition](locationbasedstatedefinition.md) <br/> |Specifies the state when it is based on location.  <br/> |
   
## Text value

The text value of the AttendeeLocation element is the attendess location.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

