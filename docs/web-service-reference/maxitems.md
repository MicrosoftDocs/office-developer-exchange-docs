---
title: "MaxItems"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: "The MaxItems element specifies the maximum number of items to return in the request."
---

# MaxItems

The **MaxItems** element specifies the maximum number of items to return in the request. 
  
```XML
<MaxItems/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetReminders](getreminders.md)
  
## Text value

The text value of the **MaxItems** element is the maximum number of items to return in the request. This number cannot be less than zero or greater than 200. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetReminders](getreminders.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

