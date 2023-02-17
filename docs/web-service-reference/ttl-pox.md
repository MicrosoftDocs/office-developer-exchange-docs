---
title: "TTL (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: "The TTL element specifies the Time to Live, in hours, during which the settings remain valid."
 
 
---

# TTL (POX)

The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.  <br/> |
   
## Text value

The text value represents the Time to Live, in hours, during which the settings remain valid. A value of zero indicates that rediscovery is not required. If no value is specified, the default value for this element is 1 hour.
  
## Remarks

After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

