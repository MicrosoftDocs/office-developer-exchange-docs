---
title: "MinimumSize"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: "The MinimumSize element represents the minimum size that a message must be in order for the condition or exception to apply."
---

# MinimumSize

The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply. 
  
```XML
<MinimumSize/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.  <br/> |
   
## Text value

The text value is an integer that identifies the minimum size of the message in bytes.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[MaximumSize](maximumsize.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

