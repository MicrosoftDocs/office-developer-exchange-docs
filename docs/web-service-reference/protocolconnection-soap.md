---
title: "ProtocolConnection (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: "The ProtocolConnection element represents the protocol connection of the server Web client."
 
 
---

# ProtocolConnection (SOAP)

The **ProtocolConnection** element represents the protocol connection of the server Web client. 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 **ProtocolConnection**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Hostname (SOAP)](hostname-soap.md) <br/> |Represents the host name portion of the full computer name of the computer.  <br/> |
|[Port (SOAP)](port-soap.md) <br/> |Represents the port number to use for the protocol.  <br/> |
|[EncryptionMethod (SOAP)](encryptionmethod-soap.md) <br/> |Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Contains zero or more protocol connections.  <br/> |
   
## Text value

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md)

