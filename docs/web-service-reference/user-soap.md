---
title: "User (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: "The User element represents the identity of a single user."
 
 
---

# User (SOAP)

The **User** element represents the identity of a single user. 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 **User**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Represents the alternate mailbox legacy distinguished name.  <br/> |
|[Mailbox (SOAP)](mailbox-soap.md) <br/> |Contains the e-mail address of the user to be discovered.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested configuration settings.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |Represents a collection of **User** elements.  <br/> |
   
## Text value

None.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

