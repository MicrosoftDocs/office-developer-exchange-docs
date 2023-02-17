---
title: "WebClientUrl (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: "The WebClientUrl element represents the URL of an Exchange web client."
 
 
---

# WebClientUrl (SOAP)

The **WebClientUrl** element represents the URL of an Exchange web client. 
  
[UserSetting (SOAP)](usersetting-soap.md)
  
[WebClientUrls (SOAP)](webclienturls-soap.md)
  
[WebClientUrl (SOAP)](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 **WebClientUrl**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AuthenticationMethods (SOAP)](authenticationmethods-soap.md) <br/> |Represents the authentication method to use when accessing the specified URL.  <br/> |
|[Url (SOAP)](url-soap.md) <br/> |Represents the web address for the URL.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[WebClientUrls (SOAP)](webclienturls-soap.md) <br/> |Represents a user setting that contains a collection of **WebClientUrl** elements.  <br/> |
   
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Url (SOAP)](url-soap.md)
  
[WebClientUrls (SOAP)](webclienturls-soap.md)

