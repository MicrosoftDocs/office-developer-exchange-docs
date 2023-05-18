---
title: "Occurrence"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: "The Occurrence element represents a single modified occurrence of a recurring calendar item."
---

# Occurrence

The **Occurrence** element represents a single modified occurrence of a recurring calendar item. 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

**OccurrenceInfoType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.  <br/> |
|[Start](start.md) <br/> |Represents the start time of a modified occurrence of a recurring calendar item.  <br/> |
|[End ](end-ex15websvcsotherref.md) <br/> |Represents the end time of a modified occurrence of a recurring calendar item.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Represents the original start time of a modified occurrence of a recurring calendar item.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

