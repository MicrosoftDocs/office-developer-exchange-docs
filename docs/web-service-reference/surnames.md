---
title: "Surnames"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 87440a49-64e2-4d97-bb1d-443c04ad24e8
description: "The Surnames element specifies an array of surname values and the identifiers of their source attributions for the associated persona."
---

# Surnames

The **Surnames** element specifies an array of surname values and the identifiers of their source attributions for the associated persona. 
  
```XML
<Surnames>
   <StringAttributedValue/>
</Surnames>
```

 **ArrayOfStringAttributedValuesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[StringAttributedValue](stringattributedvalue.md)
  
### Parent elements

[Persona](persona.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
