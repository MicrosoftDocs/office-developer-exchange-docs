---
title: "TimeZoneDefinitions"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TimeZoneDefinitions
api_type:
- schema
ms.assetid: 9ca1584e-65b8-49ba-a408-e3e8597e6607
description: "The TimeZoneDefinitions element represents an array of time zone definitions."
---

# TimeZoneDefinitions

The **TimeZoneDefinitions** element represents an array of time zone definitions. 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 **ArrayOfTimeZoneDefinitionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Specifies the periods and transitions that define a time zone.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
