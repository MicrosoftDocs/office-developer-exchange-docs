---
title: "DisableReason"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
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

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

