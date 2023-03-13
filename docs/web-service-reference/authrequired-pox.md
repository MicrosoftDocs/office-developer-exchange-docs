---
title: "AuthRequired (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 241a23ee-d2a2-4724-b794-d0d523d480a2
description: "The AuthRequired element specifies whether authentication is required."
---

# AuthRequired (POX)

The **AuthRequired** element specifies whether authentication is required. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Protocol (POX)](protocol-pox.md)
  
- [AuthRequired (POX)](authrequired-pox.md)
  
```xml
<AuthRequired>on or off</AuthRequired>
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

The text value specifies whether authentication is required. The possible values are **on** and **off**. If a value is not specified, the default value is **on**. 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

