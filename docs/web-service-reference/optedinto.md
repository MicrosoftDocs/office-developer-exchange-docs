---
title: "OptedInto"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 083a23d9-acc3-4c15-9d30-c20bf7e6808d
description: "The OptedInto element specifies a Boolean value that indicates whether the user opted in to the retention policy."
---

# OptedInto

The **OptedInto** element specifies a Boolean value that indicates whether the user opted in to the retention policy. 
  
```XML
<OptedInto>true | false</OptedInto>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[RetentionPolicyTag](retentionpolicytag.md)
  
## Text value

A text value of **true** for the **OptedInto** element indicates that the user opted in to the retention policy. A value of **false** indicates that the user did not opt into the retention policy. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

