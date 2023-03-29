---
title: "DomainName (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: "The DomainName element specifies the user's domain."
---

# DomainName (POX)

The **DomainName** element specifies the user's domain. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md)  
- [Account (POX)](account-pox.md) 
- [Protocol (POX)](protocol-pox.md) 
- [DomainName (POX)](domainname-pox.md)
  
```xml
<DomainName/>
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

The text value specifies the user's domain.
  
## Remarks

If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format. For example: \<Username\>@\<Domain\>.
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

