---
title: "MailStore (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: "The MailStore element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol."
 
 
---

# MailStore (POX)

The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[MailStore (POX)](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Client Access server.  <br/> |
   
## Remarks

The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp". 
  
The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

