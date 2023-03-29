---
title: "RedirectAddr (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: "The RedirectAddr element specifies the e-mail address that should be used for a subsequent Autodiscover request."
 
 
---

# RedirectAddr (POX)

The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[RedirectAddr (POX)](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
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
|[Account (POX)](account-pox.md) <br/> |Specifies account settings for the user.  <br/> |
   
## Text value

The text value represents the e-mail address that should be used for a subsequent Autodiscover request.
  
## Remarks

If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

