---
title: "ConnectionTimeout"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: "The ConnectionTimeout element specifies the number of minutes to keep a connection open."
---

# ConnectionTimeout

The **ConnectionTimeout** element specifies the number of minutes to keep a connection open. 
  
[GetStreamingEvents operation](getstreamingevents-operation.md)
  
[ConnectionTimeout](connectiontimeout.md)
  
```
<ConnectionTimeout/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetStreamingEvents](getstreamingevents.md) <br/> |Defines a request to get event notifications from a streaming connection.  <br/> |
   
## Text value

The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open. The value must be between 1 and 30, inclusive.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetStreamingEvents operation](getstreamingevents-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

