---
title: "LegacyDN (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: "The LegacyDN element identifies a user's mailbox by legacy distinguished name."
---

# LegacyDN (POX)

The **LegacyDN** element identifies a user's mailbox by legacy distinguished name. 
  
```xml
<LegacyDN/>
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
|[Request (POX)](request-pox.md) <br/> |Contains the request to the Autodiscover service.  <br/> |
|[User (POX)](user-pox.md) <br/> |Provides user-specific information.  <br/> |
   
## Text value

The text value represents a user's legacy e-mail address.
  
## Remarks

The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request. It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007. 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

