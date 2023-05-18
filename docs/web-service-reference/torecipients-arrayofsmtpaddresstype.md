---
title: "ToRecipients (ArrayOfSmtpAddressType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0e6fb89c-de19-48e7-af63-c41ebdf0b8e9
description: "The ToRecipients element specifies a list of recipients to whom the item was sent."
---

# ToRecipients (ArrayOfSmtpAddressType)

The **ToRecipients** element specifies a list of recipients to whom the item was sent. 
  
```XML
<ToRecipients>
   <SmtpAddress/>
</ToRecipients>
```

 **ArrayOfSmtpAddressType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[SmtpAddress](smtpaddress.md)
  
### Parent elements

[SearchPreviewItem](searchpreviewitem.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

