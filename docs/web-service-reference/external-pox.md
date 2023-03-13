---
title: "External (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: "The External element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network."
 
 
---

# External (POX)

The **External** element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[External (POX)](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed. This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.  <br/> |
   
## Remarks

The **External** element is an optional child element of the **Protocol** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

