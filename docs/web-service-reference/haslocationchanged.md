---
title: "HasLocationChanged"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: "The HasLocationChanged element specifies whether the location property of a meeting has changed."
---

# HasLocationChanged

The **HasLocationChanged** element specifies whether the location property of a meeting has changed. 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
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

A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed. A value **false** indicates that the location property of a meeting has not changed. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Code**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

