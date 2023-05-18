---
title: "People"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 65312428-548c-4fe9-971a-d0dab3be5ddf
description: "The People element specifies an array of persona data returned as the result of a FindPeople request."
---

# People

The **People** element specifies an array of persona data returned as the result of a **FindPeople** request. 
  
```XML
<People>
   <Persona/>
</People>
```

**ArrayOfPeopleType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Persona](persona.md)
  
### Parent elements

[FindPeopleResponse](findpeopleresponse.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

