---
title: "ConvertHtmlCodePageToUTF8"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: "The ConvertHtmlCodePageToUTF8 element indicates whether the item HTML body is converted to UTF8."
---

# ConvertHtmlCodePageToUTF8

The **ConvertHtmlCodePageToUTF8** element indicates whether the item HTML body is converted to UTF8. 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 **xs:boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifies a set of properties to return in a response.  <br/> |
   
## Text value

A text value of **true** for the **ConvertHtmlCodePageToUTF8** element indicates that the HTML body is converted to UTF8. A text value of **false** indicates that the HTML body is not converted to UTF8. 
  
## Remarks

The default value of **true** is used if the **ConvertHtmlCodePageToUTF8** element is not specified in a request. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

