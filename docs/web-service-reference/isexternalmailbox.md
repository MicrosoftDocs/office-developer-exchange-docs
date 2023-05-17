---
title: "IsExternalMailbox"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: "The IsExternalMailbox element indicates whether the mailbox is external to the organization."
---

# IsExternalMailbox

The **IsExternalMailbox** element indicates whether the mailbox is external to the organization. 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SearchableMailbox](searchablemailbox.md)
  
## Text value

A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization. A value of **false** indicates that the mailbox is in the organization. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

