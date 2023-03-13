---
title: "DeploymentId (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: "The DeploymentId element uniquely identifies the Microsoft Exchange Server 2007 forest."
---

# DeploymentId (POX)

The **DeploymentId** element uniquely identifies the Microsoft Exchange Server 2007 forest. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md) 
- [User (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[User (POX)](user-pox.md) <br/> |Provides user-specific information.  <br/> |
   
## Text value

The text value uniquely identifies the Exchange 2007 forest in GUID format.
  
## Remarks

If you uninstall and then reinstall Exchange 2007 and you use the same server name, the **DeploymentId** value changes. 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

