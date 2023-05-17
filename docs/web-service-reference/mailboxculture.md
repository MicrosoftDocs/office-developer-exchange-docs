---
title: "MailboxCulture"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailboxCulture
api_type:
- schema
ms.assetid: 105cc061-3c35-455f-b102-8023e2055632
description: "The MailboxCulture element indicates the culture to use when opening a mailbox. This element occurs in the SOAP header."
---

# MailboxCulture

The **MailboxCulture** element indicates the culture to use when opening a mailbox. This element occurs in the SOAP header. 
  
```xml
<MailboxCulture/>
```

**MailboxCultureType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

None.
  
## Text value

The text value indicates the language that is used in the Exchange Web Service operations. The possible values for this element are described by RFC 3066.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

