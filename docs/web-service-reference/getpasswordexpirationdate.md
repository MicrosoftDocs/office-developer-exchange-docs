---
title: "GetPasswordExpirationDate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: "The GetPasswordExpirationDate element defines a request to get the password expiration date for an email account. This element is the base element for the GetPasswordExpirationDate operation operation."
---

# GetPasswordExpirationDate

The **GetPasswordExpirationDate** element defines a request to get the password expiration date for an email account. This element is the base element for the [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation. 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 **GetPasswordExpirationDateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element name**|**Description**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Represents the email address of the email account for which the password expiration date is to be returned.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

