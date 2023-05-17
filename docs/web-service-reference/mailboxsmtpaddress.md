---
title: "MailboxSmtpAddress"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: "The MailboxSmtpAddress element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved."
---

# MailboxSmtpAddress

The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved. 
  
```XML
<MailboxSmtpAddress/>
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
|[GetInboxRules](getinboxrules.md) <br/> |Defines a request to get the Inbox rules on a mailbox in the server store.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Defines a request to get the password expiration date of an email account.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Defines a request to update the Inbox rules in a mailbox in the server store.  <br/> |
   
## Text value

None.
  
## Remarks

The **MailboxSmtpAddress** element is an optional element. If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetInboxRules operation](getinboxrules-operation.md)
- [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md)
- [UpdateInboxRules operation](updateinboxrules-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

