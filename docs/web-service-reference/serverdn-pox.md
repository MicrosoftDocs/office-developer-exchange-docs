---
title: "ServerDN (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: "The ServerDN element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007."
 
 
---

# ServerDN (POX)

The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[ServerDN (POX)](serverdn-pox.md)
  
```xml
<ServerDN/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.  <br/> |
   
## Text value

The text value represents the distinguished name of the Exchange server.
  
## Remarks

The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

