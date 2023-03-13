---
title: "User (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: "The User element provides user-specific information."
 
 
---

# User (POX)

The **User** element provides user-specific information. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[User (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DisplayName (string)](displayname-string.md) <br/> |Represents the user's display name.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifies a user's mailbox by legacy distinguished name.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Uniquely identifies the Exchange forest.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Contains the user's SMTP address that is used for the Autodiscover process.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Contains the response from the Autodiscover service.  <br/> |
   
## Remarks

Autodiscover requests and responses must be UTF-8 encoded.
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

