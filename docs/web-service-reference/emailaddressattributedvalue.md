---
title: "EmailAddressAttributedValue"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: "The EmailAddressAttributedValue element specifies an instance of an array of email addresses and their associated attributions."
---

# EmailAddressAttributedValue

The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions. 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Value (EmailAddressType)](value-emailaddresstype.md) <br/> |Specifies the value of an **EmailAddress** associated with an attributions array.  <br/> |
|[Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Specifies an array of attributions for its associated **Value** element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Specifies an array of email values and the identifiers of their source attributions for the associated persona.  <br/> |
|[Emails2](emails2.md) <br/> |Specifies an array of email values and the identifiers of their source attributions for the associated persona.  <br/> |
|[Emails3](emails3.md) <br/> |Specifies an array of email values and the identifiers of their source attributions for the associated persona.  <br/> |
   
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

