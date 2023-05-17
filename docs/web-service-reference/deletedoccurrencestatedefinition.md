---
title: "DeletedOccurrenceStateDefinition"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: "The DeletedOccurrenceStateDefinition specifies the state for a deleted occurrence of a calendar item."
---

# DeletedOccurrenceStateDefinition

The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item. 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 **DeletedOccurrenceStateDefinitionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Occurrence (Time Zone Transition)](occurrence-time-zone-transition.md) <br/> |Specifies the date of the occurrence of a calendar item.  <br/> |
|[IsOccurrencePresent](isoccurrencepresent.md) <br/> |Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[StateDefinition](statedefinition.md) <br/> |Specifies a state definition.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

