---
title: "PrincipalName"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: "The PrincipalName element represents the user principal name (UPN) of the account to be used for Exchange impersonation."
---

# PrincipalName

The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation. 
  
```xml
<PrincipalName/>
```

 **PrincipalNameType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.  <br/> The following is the XPath expression to this element:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## Text value

The text value represents the UPN of a user. This value exists on the user object in the Active Directory directory service. This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Server-to-server authorization in EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

