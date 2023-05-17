---
title: "Description"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 6e4cd194-0696-4fec-8ab0-e1d349ed0be0
description: "The Description element specifies the descriptive text for the retention policy."
---

# Description

The **Description** element specifies the descriptive text for the retention policy. 
  
```XML
<Description></Description>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RetentionPolicyTag](retentionpolicytag.md) <br/> |Specifies the retention policy for a mailbox item.  <br/> |
   
## Text value

The text value of the **Description** element is a string value that describes the retention policy. 
  
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

