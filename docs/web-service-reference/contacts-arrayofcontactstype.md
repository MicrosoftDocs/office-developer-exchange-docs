---
title: "Contacts (ArrayOfContactsType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e
description: "The Contacts element specifies an array of contacts."
---

# Contacts (ArrayOfContactsType)

The **Contacts** element specifies an array of contacts. 
  
```XML
<Contacts>
    <Contact></Contact>
</Contacts>
```

 **ArrayOfContactsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Contact (ContactType)](contact-contacttype.md) <br/> |Specifies a contact in the Unified Contact Store.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |Specifies the **EntityExtractionResult** property of an item.  <br/> |
   
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

