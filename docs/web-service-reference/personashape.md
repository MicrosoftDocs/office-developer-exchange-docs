---
title: "PersonaShape"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 61d87cd5-3270-40d1-bab7-d0d5bf938607
description: "The PersonaShape element specifies the set of persona properties to be returned from a FindPeople request."
---

# PersonaShape

The **PersonaShape** element specifies the set of persona properties to be returned from a **FindPeople** request. 
  
```XML
<PersonaShape>
   <BaseShape/>
   <AdditionalProperties/>
</PersonaShape>
```

 **PersonaResponseShapeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[BaseShape](baseshape.md) | [AdditionalProperties](additionalproperties.md)
  
### Parent elements

[FindPeople](findpeople.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

