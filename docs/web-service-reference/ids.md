---
title: "Ids"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Ids
api_type:
- schema
ms.assetid: c54cdeaf-6761-4d1a-a329-fb279f0e2a64
description: "The Ids element contains an array of time zone definition identifiers."
---

# Ids

The **Ids** element contains an array of time zone definition identifiers. 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 **NonEmptyArrayOfTimeZoneIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Id (TimeZone)](id-timezone.md) <br/> |The element that identifies a single time zone definition.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetServerTimeZones](getservertimezones.md) <br/> |Defines a request to retrieve time zone definitions from the Exchange server.  <br/> |
   
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

