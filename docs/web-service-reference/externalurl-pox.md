---
title: "ExternalUrl (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: "The ExternalUrl element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol."
 
 
---

# ExternalUrl (POX)

The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol. 
  
```XML
<ExternalUrl/>
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.  <br/> |
   
## Text value

The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.
  
## Remarks

The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp". 
  
The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

