---
title: "EcpUrl-tmEditing (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: "The EcpUrl-tmEditing element specifies a partial URL that can be combined with the EcpUrl (POX) element's value to generate a URL that can be used to edit an existing site mailbox."
 
 
---

# EcpUrl-tmEditing (POX)

The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.  <br/> |
   
## Text value

The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox. The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table. 
  
|**Parameter**|**Substitute with**|
|:-----|:-----|
| _Id_ <br/> |The SMTP email address or the X500 distinguished name of the site mailbox.  <br/> |
   
## Remarks

The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

