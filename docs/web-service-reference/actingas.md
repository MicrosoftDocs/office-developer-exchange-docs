---
title: "ActingAs"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: "The ActingAs element identifies who the caller is sending as."
---

# ActingAs

The **ActingAs** element identifies who the caller is sending as. 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 **EmailAddressType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetServiceConfiguration](getserviceconfiguration.md) <br/> |Defines a **GetServiceConfiguration** request.  <br/> |
   
## Remarks

This element is optional. If this element is not present, the authenticated user is assumed to be the sender. The **ActingAs** element must be included for requesting sender hints. An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

