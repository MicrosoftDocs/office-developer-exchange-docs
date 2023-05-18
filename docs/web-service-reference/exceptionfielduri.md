---
title: "ExceptionFieldURI"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: "The ExceptionFieldURI element identifies particular errors in a request. This element is only used as part of an error response in the MessageXml node."
---

# ExceptionFieldURI

The **ExceptionFieldURI** element identifies particular errors in a request. This element is only used as part of an error response in the [MessageXml](messagexml.md) node. 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**FieldURI** <br/> |Identifies a property of an occurrence of a recurring item. This attribute is required.  <br/> |
   
#### FieldURI Attribute

|**Value**|**Description**|
|:-----|:-----|
|attachment:Name  <br/> |Identifies the attachment name as containing an error.  <br/> |
|attachment:ContentType  <br/> |Identifies the content type as containing an error.  <br/> |
|attachment:Content  <br/> |Identifies the content as containing an error.  <br/> |
|recurrence:Month  <br/> |Identifies the month field as containing an error.  <br/> |
|recurrence:DayOfWeekIndex  <br/> |Identifies the day of week index as containing an error.  <br/> |
|recurrence:DaysOfWeek  <br/> |Identifies the DaysOfWeek property as containing an error.  <br/> |
|recurrence:DayOfMonth  <br/> |Identifies the DayOfMonth as containing an error.  <br/> |
|recurrence:Interval  <br/> |Identifies the interval as containing an error.  <br/> |
|recurrence:NumberOfOccurrences  <br/> |Identifies the number of occurrences as containing an error.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

