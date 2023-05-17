---
title: "TimeZoneDefinition"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: "The TimeZoneDefinition element specifies the periods and transitions that define a time zone."
---

# TimeZoneDefinition

The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone. 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Represents the unique identifier of the time zone.  <br/> |
|Name  <br/> |Represents the descriptive name of the time zone.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Periods](periods.md) <br/> |Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.  <br/> |
|[Transitions](transitions.md) <br/> |Represents an array of time zone transitions.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Represents an array of time zone definitions.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).  <br/> |
   
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

