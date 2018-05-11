---
title: "ConnectingSID"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: "The ConnectingSID element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header."
---

# ConnectingSID

The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header. 
  
[ExchangeImpersonation](exchangeimpersonation.md)
  
[ConnectingSID](connectingsid.md)
  
```
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

 **ConnectingSIDType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |Represents the user principal name (UPN) of the account to use for impersonation. This should be the UPN for the domain where the user account exists.  <br/> |
|[SID](sid.md) <br/> |Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation. If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user. We recommend that you use the SID or UPN if they are available.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation. If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user. We recommend that you use the SID or UPN if they are available.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Used in the SOAP header of a request. When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.  <br/> The following is the XPath expression to this element:  <br/>  `/ExchangeImpersonation` <br/> |
   
## Remarks

The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Other resources

[Server-to-server authorization in EWS](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

