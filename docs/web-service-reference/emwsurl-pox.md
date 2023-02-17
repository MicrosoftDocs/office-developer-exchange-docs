---
title: "EmwsUrl (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: "The EmwsUrl element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user."
---

# EmwsUrl (POX)

The **EmwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user. 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md) 
- [Account (POX)](account-pox.md) 
- [Protocol (POX)](protocol-pox.md) 
- [EmwsUrl (POX)](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
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

The text value represents the URL of the EWS endpoint for the user. It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element. 
  
## Remarks

The **EmwsUrl** element is an optional child element of the **Protocol** element. 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

