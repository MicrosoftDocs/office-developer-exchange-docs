---
title: "Type (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: "The Type element identifies the type of the configured mail account."
 
 
---

# Type (POX)

The **Type** element identifies the type of the configured mail account. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Type (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Exchange server.  <br/> |
   
## Text value

The text value represents the type of mail account. The following table lists the possible values.
  
|**Value**|**Description**|
|:-----|:-----|
|EXCH  <br/> |The protocol that is used to connect to the server is Exchange RPC.  <br/> |
|EXHTTP  <br/> |The protocol that is used to connect to the server RPC/HTTP connections.  <br/> |
|EXPR  <br/> |The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.  <br/> This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.  <br/> |
|WEB  <br/> |E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.  <br/> This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.  <br/> |
   
### Version differences

Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo". 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

