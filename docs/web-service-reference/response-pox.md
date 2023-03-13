---
title: "Response (POX)"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 002b72f2-f94d-467c-8e6c-b3818f7e51dc
description: "Applies to:"
 
 
---

# Response (POX)


  
The **Response** element contains the response from the Autodiscover service. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
```xml
<Response>
   <User/>
   <Account/>
</Response>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[User (POX)](user-pox.md) <br/> |Provides user-specific information. This element is optional.  <br/> |
|[Account (POX)](account-pox.md) <br/> |Specifies account settings for the user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AutoDiscover (POX)](autodiscover-pox.md) <br/> |The root element in an Autodiscover response.  <br/> |
   
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

