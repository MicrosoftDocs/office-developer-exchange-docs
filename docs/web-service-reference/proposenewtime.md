---
title: "ProposeNewTime"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6d5977ac-484e-4e53-92ba-58a868eb3395
description: "The ProposeNewTime element specifies a response object that indicates that the meeting attendee can propose a new meeting time."
---

# ProposeNewTime

The **ProposeNewTime** element specifies a response object that indicates that the meeting attendee can propose a new meeting time. 
  
```XML
<ProposeNewTime ObjectName=""></ProposeNewTime>
```

 **ProposeNewTimeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

****

|**Attribute**|**Description**|
|:-----|:-----|
|ObjectName  <br/> |The name of the response object.  <br/> |
   
#### Child elements

None.
  
#### Parent elements

[ResponseObjects](responseobjects.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

#### Reference

[ResponseObjects](responseobjects.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

