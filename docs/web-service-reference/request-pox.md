---
title: "Request (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: "The Request element contains the request to the Autodiscover service."
---

# Request (POX)

The **Request** element contains the request to the Autodiscover service. 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Request (POX)](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Identifies the schema for an Autodiscover response.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Identifies the user's e-mail address.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifies a user's mailbox by legacy distinguished name.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AutoDiscover (POX)](autodiscover-pox.md) <br/> |The root element in an Autodiscover request.  <br/> |
   
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

