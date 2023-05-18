---
title: "Children (ArrayOfStringArrayAttributedValuesType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: "The Children element specifies an array of child names and identifiers of their source attributions for the associated persona."
---

# Children (ArrayOfStringArrayAttributedValuesType)

The **Children** element specifies an array of child names and identifiers of their source attributions for the associated persona. 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 **ArrayOfStringArrayAttributedValuesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Specifies an instance of an array of string data for a persona element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Specifies a set of persona data returned by a **GetPersona** request.  <br/> |
   
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

