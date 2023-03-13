---
title: "EcpUrl-tm (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 3f35d5ac-55be-4d3a-ad03-7d6e9349d923
description: "The EcpUrl-tm element specifies a partial URL that can be combined with the EcpUrl (POX) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member."
 
 
---

# EcpUrl-tm (POX)

The **EcpUrl-tm** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-tm (POX)](ecpurl-tm-pox.md)
  
```XML
<EcpUrl-tm/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.  <br/> |
   
## Text value

The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of site mailboxes for the user. 
  
## Remarks

The **EcpUrl-tm** element is an optional child element of the **Protocol** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

