---
title: "TTL (ClientAccessTokenTypeType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: cc8f8caa-fced-49b6-9861-d112590b218a
description: "The TTL element indicates the time to live value for the token."
---

# TTL (ClientAccessTokenTypeType)

The **TTL** element indicates the time to live value for the token. 
  
```XML
<TTL></TTL>
```

 **integer**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[TokenRequest](tokenrequest.md) | [Token](token.md)
  
## Text value

The text value for the **TTL** element indicates how long the token remains valid. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

