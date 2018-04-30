---
title: "HomePhones2"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
ms.assetid: ba9bb159-362d-48e0-889d-823cb46ecebf
description: "The HomePhones2 element specifies an array of HomePhone2 values and the identifiers of their source attributions for the associated persona."
---

# HomePhones2

The **HomePhones2** element specifies an array of **HomePhone2** values and the identifiers of their source attributions for the associated persona. 
  
```XML
<HomePhones2>
    <PhoneNumberAttributedValue/>
</HomePhones2>
```

 **ArrayOfPhoneNumberAttributedValuesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Contains a single attributed phone number for a persona.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Specifies a set of persona data returned by a **GetPersona** request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

