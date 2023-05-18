---
title: "TransitionsGroup"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TransitionsGroup
api_type:
- schema
ms.assetid: 19d56080-546a-4d53-929e-363d56186759
description: "The TransitionsGroup element represents an array of time zone transitions."
---

# TransitionsGroup

The **TransitionsGroup** element represents an array of time zone transitions. 
  
```xml
<TransitionsGroup Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 **ArrayOfTransitionsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |A string value that represents the unique identifier of the transitions group.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Represents a time zone transition that occurs on a specific date and at a specific time.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Represents a time zone transition that occurs on the same day each year.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Represents a time zone transition that occurs on a specified day of the year.  <br/> |
|[Transition](transition.md) <br/> |Represents a time zone transition.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TransitionsGroups](transitionsgroups.md) <br/> |Represents an array of time zone transition groups.  <br/> |
   
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

