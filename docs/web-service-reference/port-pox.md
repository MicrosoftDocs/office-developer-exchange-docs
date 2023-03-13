---
title: "Port (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4046821a-d6f3-4764-82be-4011221ce7a3
description: "The Port element specifies the port that is used to connect to the store."
 
 
---

# Port (POX)

The **Port** element specifies the port that is used to connect to the store. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Port (POX)](port-pox.md)
  
```xml
<Port/>
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

The text value represents the port that is used to access the Exchange server.
  
## Remarks

The **Port** value is not used if the [Server (POX)](server-pox.md) element contains a URL. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

