---
title: "TokenRequest"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 54f45f8e-c02b-4ead-b15a-38b30872c362
description: "The TokenRequest element specifies a single token request."
---

# TokenRequest

The **TokenRequest** element specifies a single token request. 
  
```XML
<TokenRequest>
   <Id/>
   <TokenType/>
</TokenRequest>
```

 **ClientAccessTokenRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ID (String)](id-string.md) | [TokenType (ClientAccessTokenType)](tokentype-clientaccesstokentype.md)
  
### Parent elements

[TokenRequests](tokenrequests.md)
  
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
