---
title: "NormalizedBodyType"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: "The NormalizedBodyType element specifies whether the normalized body is returned in text or HTML format."
---

# NormalizedBodyType

The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format. 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 **BodyTypeResponseType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ItemShape](itemshape.md)
  
## Text value

The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in. The following table lists the possible values for this element. 
  
****

|**Value**|**Description**|
|:-----|:-----|
|Best  <br/> |The response will return the richest available content of body text. This is useful if it is unknown whether the content is text or HTML.  <br/> The returned body will be text if the stored body is plain text. Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.  <br/> This is the default value.  <br/> |
|HTML  <br/> |The response will return a normalized body as HTML.  <br/> |
|Text  <br/> |The response will return a normalized body as plain text.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[ItemShape](itemshape.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

