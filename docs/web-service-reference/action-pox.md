---
title: "Action (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: "The Action element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information."
---

# Action (POX)

The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Action (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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

The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information. The following table lists the possible values.
  
|**Value**|**Description**|
|:-----|:-----|
|redirectUrl  <br/> |If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request. The client application should stop redirecting after 10 redirects.  <br/> |
|redirectAddr  <br/> |If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.  <br/> |
|settings  <br/> |If this value is specified, the Autodiscover response contains settings that are used to configure the account. Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.  <br/> |
   
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

