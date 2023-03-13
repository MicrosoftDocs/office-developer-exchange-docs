---
title: "OWAUrl (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: "The OWAUrl element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access."
 
 
---

# OWAUrl (POX)

The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Internal (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |Describes the authentication methods for accessing Outlook Web Access.  <br/> |
   
#### AuthenticationMethod Attribute

|**Value**|**Description**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Integrated Windows authentication.  <br/> |
|FBA  <br/> |Forms-based authentication.  <br/> |
|NTLM  <br/> |NTLM authentication.  <br/> |
|Digest  <br/> |Digest authentication.  <br/> |
|Basic  <br/> |Basic authentication.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Internal (POX)](internal-pox.md) <br/> |Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.  <br/> |
   
## Text value

The text value represents the URL for the Outlook Web Access service on a Client Access server.
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

