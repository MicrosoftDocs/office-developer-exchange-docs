---
title: "SmtpAddress (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: "The SmtpAddress element contains the SMTP address assigned to the public folder message store configured for the user."
---

# SmtpAddress (POX)

The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
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
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.  <br/> |
   
## Text value

The text value represents the SMTP address assigned to the public folder store configured for the user. This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings. 
  
## Remarks

The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element. 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

