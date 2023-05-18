---
title: "To"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: "The To element specifies the target of the time zone transition. The target is either a time zone period or a group of time zone transitions."
---

# To

The **To** element specifies the target of the time zone transition. The target is either a time zone period or a group of time zone transitions. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Kind  <br/> |Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.  <br/> |
   
#### Kind attribute values

|**Value**|**Description**|
|:-----|:-----|
|Period  <br/> |Specifies that the time zone transition target is a time zone period.  <br/> |
|Group  <br/> |Specifies that the time zone transition target is a group of time zone transitions.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Represents a time zone transition that occurs on a specific date and at a specific time.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Represents a time zone transition that occurs on the same day each year.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Represents a time zone transition that occurs on a specified day of the year.  <br/> |
|[Transition](transition.md) <br/> |Represents a time zone transition.  <br/> |
   
## Text value

The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition. 
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

