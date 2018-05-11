---
title: "TokenType (ClientAccessTokenType)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: "The TokenType element identifies the type of client access token that will be returned in the GetClientAccessToken response."
---

# TokenType (ClientAccessTokenType)

The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response. 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)
  
## Text value

A text value of **CallerIdentity** means a caller identity client access token is returned. A text value of **ExtensionCallback** indicates that an extension callback client access token is returned. A text value of **ScopedToken** indicates that the client access token is a scoped token. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

