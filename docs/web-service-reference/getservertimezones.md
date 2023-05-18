---
title: "GetServerTimeZones"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: "The GetServerTimeZones element is the root element in a request to retrieve time zone definitions from the Exchange server."
---

# GetServerTimeZones

The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone. This attribute is optional. The default value is **true**.  <br/> |
   
#### ReturnFullTimeZoneData Attribute

|**Value**|**Description**|
|:-----|:-----|
|**true** <br/> |Return the complete definitions for each time zone.  <br/> |
|**false** <br/> |Return only the name and identifier for each time zone.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Ids](ids.md) <br/> |Contains an array of time zone definition identifiers that specifies the requested time zone definitions. This element is optional. If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetServerTimeZones operation](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

