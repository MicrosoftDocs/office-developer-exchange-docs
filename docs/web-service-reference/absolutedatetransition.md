---
title: "AbsoluteDateTransition"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AbsoluteDateTransition
api_type:
- schema
ms.assetid: 8f5731eb-bed0-45bf-ba89-4aaf20c34a39
description: "The AbsoluteDateTransition element represents a time zone transition that occurs on a specific date and at a specific time."
---

# AbsoluteDateTransition

The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time. 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

**AbsoluteDateTransitionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[To](to.md) <br/> |Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.  <br/> |
|[DateTime](datetime.md) <br/> |Represents the date and time at which the time zone transition occurs.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |Represents a collection of time zone transitions.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Represents a collection of time zone transitions.  <br/> |
   
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

