---
title: "AuthenticationMethods (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ae97c802-f6ef-46da-b774-ca0a5feb664f
description: "The AuthenticationMethods element describes the authentication methods that are available for a Web client."
---

# AuthenticationMethods (SOAP)

The **AuthenticationMethods** element describes the authentication methods that are available for a Web client. 
  
```XML
<AuthenticationMethods/>
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
|[WebClientUrl (SOAP)](webclienturl-soap.md) <br/> |Represents the URL of the Outlook Web App client.  <br/> |
   
## Text value

The text value of the **AuthenticationMethods** element is the URL of the Outlook Web App client. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)

