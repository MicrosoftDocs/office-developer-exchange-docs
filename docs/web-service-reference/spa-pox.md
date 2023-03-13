---
title: "SPA (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: fba018d5-0c65-4e1b-9767-d1ce8b356278
description: "The SPA element indicates whether Secure Password Authentication (SPA) is required."
 
 
---

# SPA (POX)

The **SPA** element indicates whether Secure Password Authentication (SPA) is required. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[SPA (POX)](spa-pox.md)
  
```xml
<SPA/>
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

The text value indicates whether SPA is required. If the text value is **on**, SPA is required.
  
## Remarks

If this element is not present, the default value is set to **on**.
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

