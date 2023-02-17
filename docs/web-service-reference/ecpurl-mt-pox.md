---
title: "EcpUrl-mt (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: "The EcpUrl-mt element specifies a partial URL that can be combined with the EcpUrl (POX) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user."
 
 
---

# EcpUrl-mt (POX)

The **EcpUrl-mt** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-mt (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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

The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email tracking settings for the user. The value of the **EcpUrl-mt** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table. 
  
|**Parameter**|**Substitute with**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _MsgID_ <br/> |Internet message identifier of the message to be tracked as specified by the Message-ID header.  <br/> |
| _Mbx_ <br/> |The SMTP address of the mailbox owner.  <br/> |
| _Sender_ <br/> |The SMTP address of the message's sender.  <br/> |
   
## Remarks

The **EcpUrl-mt** element is an optional child element of the **Protocol** element. 
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

