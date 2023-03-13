---
title: "PublicFolderInformation (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: "The PublicFolderInformation element contains information that clients can use to send an Autodiscover request to discover public folder information for the user."
 
 
---

# PublicFolderInformation (POX)

The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SmtpAddress (POX)](smtpaddress-pox.md) <br/> |Contains the SMTP address assigned to the public folder message store configured for the user. This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |Specifies account settings for the user.  <br/> |
   
## Remarks

The **PublicFolderInformation** element is an optional child element of the **Account** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

