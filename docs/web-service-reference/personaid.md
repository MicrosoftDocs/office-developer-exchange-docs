---
title: "PersonaId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: "The PersonaId element specifies the persona identifier for the associated persona."
---

# PersonaId

The **PersonaId** element specifies the persona identifier for the associated persona. 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The text value of the **Id** attribute is the identifier of the persona.  <br/> |
|ChangeKey  <br/> |The text value of the **ChangeKey** attribute is the change key of the persona.  <br/> |
   
### Child elements

None.
  
### Parent elements

[GetPersona](getpersona.md) | [Persona](persona.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

