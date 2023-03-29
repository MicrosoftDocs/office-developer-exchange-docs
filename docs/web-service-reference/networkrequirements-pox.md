---
title: "NetworkRequirements (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: "The NetworkRequirements element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server."
 
 
---

# NetworkRequirements (POX)

The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[NetworkRequirements (POX)](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.  <br/> |
   
## Remarks

If the e-mail client does not match the network requirements, it should try other protocol types. ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network. ISPs may list another set of servers that require authentication but are not required to be on a specific network. 
  
The **NetworkRequirements** element is optional. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

