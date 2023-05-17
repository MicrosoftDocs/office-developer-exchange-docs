---
title: "MaximumSize"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: "The MaximumSize element represents the maximum size that a message must be in order for the condition or exception to apply."
---

# MaximumSize

The **MaximumSize** element represents the maximum size that a message must be in order for the condition or exception to apply. 
  
```XML
<Maximum/>
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

The text value is an integer that identifies the maximum size of the message in bytes.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[MinimumSize](minimumsize.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

