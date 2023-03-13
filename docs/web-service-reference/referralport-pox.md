---
title: "ReferralPort (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: "The ReferralPort element specifies the port that is used to get a referral to a directory."
 
 
---

# ReferralPort (POX)

The **ReferralPort** element specifies the port that is used to get a referral to a directory. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[ReferralPort (POX)](referralport-pox.md)
  
```xml
<ReferralPort/>
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

The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

