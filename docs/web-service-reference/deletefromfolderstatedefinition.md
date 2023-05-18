---
title: "DeleteFromFolderStateDefinition"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3aba59a0-f12a-48b5-842b-11cf4530dd51
description: "The DeleteFromFolderStateDefinition element specifies the state when an item is deleted from a folder."
---

# DeleteFromFolderStateDefinition

The **DeleteFromFolderStateDefinition** element specifies the state when an item is deleted from a folder. 
  
```XML
<DeleteFromFolderStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeleteFromFolderStateDefinition>
```

 **DeleteFromFolderStateDefinitionType**
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

