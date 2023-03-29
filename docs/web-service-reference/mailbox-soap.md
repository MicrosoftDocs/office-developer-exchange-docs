---
title: "Mailbox (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4ad59e5b-4047-4c34-a318-ca06c31d3de8
description: "The Mailbox element contains the e-mail address of the user to be discovered."
---

# Mailbox (SOAP)

The **Mailbox** element contains the e-mail address of the user to be discovered. 
  
```XML
<Mailbox/>
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
|[User (SOAP)](user-soap.md) <br/> |Represents the identity of a single user.  <br/> |
   
## Text value

The text value of the **Mailbox** element is the e-mail address of the user to be discovered. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)

