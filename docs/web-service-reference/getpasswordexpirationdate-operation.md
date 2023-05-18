---
title: "GetPasswordExpirationDate operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: "The GetPasswordExpirationDate operation provides the email account password expiration date for the current user."
---

# GetPasswordExpirationDate operation

The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user. 
  
This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## GetPasswordExpirationDate operation SOAP headers

The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table. 
  
|**Header**|**Element**|**Description**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox. This is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema for the operation request. This is applicable to a request. This is applicable to a request.  <br/> |
   
## GetPasswordExpirationDate operation request example

### Description

The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account. 
  
### Code

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### Request elements

The following elements are used in the request:
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## Successful GetPasswordExpirationDate operation response

The following elements are used in the response:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

