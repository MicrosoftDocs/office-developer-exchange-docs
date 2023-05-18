---
title: "InternalDomains (SmtpDomainList)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InternalDomains
api_type:
- schema
ms.assetid: 0f2cbb05-338d-4302-8871-a06e78b33f98
description: "The InternalDomains element identifies the list of internal SMTP domains of the organization."
---

# InternalDomains (SmtpDomainList)

The **InternalDomains** element identifies the list of internal SMTP domains of the organization. 
  
```XML
<InternalDomains>
   <Domain/>
</InternalDomains>
```

 **SmtpDomainList**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domain](domain.md) <br/> |Identifies a single SMTP domain.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Contains service configuration information for the mail tips service.  <br/> |
|[ProtectionRulesConfiguration](protectionrulesconfiguration.md) <br/> |Contains service configuration information for the protection rules service.  <br/> |
   
## Text value

None.
  
## Remarks

This element is required. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

