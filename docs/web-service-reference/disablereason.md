---
title: "DisableReason"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: "The DisableReason element specifies the reason for disabling an app."
---

# DisableReason

The **DisableReason** element specifies the reason for disabling an app. 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 **DisableReasonType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DisableApp](disableapp.md) <br/> |Specifies a request to disable an app.  <br/> |
   
## Text value

**DisableReason element text value**

|**Value**|**Description**|
|:-----|:-----|
|NoReason  <br/> |No reason given  <br/> |
|OutlookClientPerformance  <br/> |To improve email client performance.  <br/> |
|OWAClientPerformance  <br/> |To improve Web app client performance.  <br/> |
|MobileClientPerformance  <br/> |To improve mobile client performance.  <br/> |
   
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

