---
title: "AddressBook (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: "The AddressBook element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol."
 
 
---

# AddressBook (POX)

The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[AddressBook (POX)](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Client Access server.  <br/> |
   
## Remarks

The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp". 
  
The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

