---
title: "FileAsIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 71cae100-b68e-454b-b9b6-ddbcb4d78f3f
description: "The FileAsIds element specifies an array of StringAttributedValue elements and the identifiers of their source attributions for the associated persona."
---

# FileAsIds

The **FileAsIds** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona. 
  
```XML
<FileAsIds>
    <StringAttributedValue/>
<FileAsIds>
```

 **ArrayOfStringAttributedValuesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |Specifies an instance in an array of attributes associated with a persona element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Specifies a set of persona data returned by a **GetPersona** request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

