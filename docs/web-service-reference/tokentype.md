---
title: "TokenType" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: "The TokenType element specifies the type of token."
---

# TokenType

The **TokenType** element specifies the type of token. 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 **ClientAccessTokenTypeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[TokenRequest](tokenrequest.md) | [Token](token.md)
  
## Text value

The text value of the **TokenType** element is the token type. The text value of **CallerIdentity** indicates that the token is a caller identity token. The text value of **ExtensionCallback** indicates that the token is for an extension callback. The text value of **ScopedToken** indicates that the client access token is a scoped token. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| **Element** | **Example** |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
