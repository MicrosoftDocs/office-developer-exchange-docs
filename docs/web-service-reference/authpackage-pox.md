---
title: "AuthPackage (POX)"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: "The AuthPackage element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed."
---

# AuthPackage (POX)

The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Protocol (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Client Access server.  <br/> |
   
## Text value

The text value specifies the authentication scheme that is used when authenticating against the Mailbox server. The following are the possible values:
  
- basic
- kerb
- kerbntlm
- ntlm
- certificate
- negotiate
- nego2
    
## Remarks

The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR. 
  
### Version differences

Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate". 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

