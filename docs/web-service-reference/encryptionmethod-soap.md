---
title: "EncryptionMethod (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bc632c85-ec74-4a00-baec-df5973e032fa
description: "The EncryptionMethod element represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols."
---

# EncryptionMethod (SOAP)

The **EncryptionMethod** element represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols. 
  
```XML
<EncryptionMethod/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ProtocolConnection (SOAP)](protocolconnection-soap.md) <br/> |Represents the protocol connection of the server Web client.  <br/> |
   
## Text value

The text value for this element is the cryptographic method that is used for the POP, IMAP, and SMTP protocols.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)

