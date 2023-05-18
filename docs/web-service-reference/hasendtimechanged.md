---
title: "HasEndTimeChanged"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: "The HasEndTimeChanged element specifies whether the end time for a meeting has changed."
---

# HasEndTimeChanged

The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed. 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ChangeHighlights](changehighlights.md) <br/> |Specifies what has changed between two versions of a meeting request message.  <br/> |
   
## Text value

A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed. A value of **false** indicates that the end time of a meeting has not changed. 
  
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

