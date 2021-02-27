---
title: "Identify the account to impersonate"
 
 
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
 
 
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: "Learn how your service application uses EWS to identify the user to impersonate."
localization_priority: Priority
---

# Identify the account to impersonate

Learn how your service application uses EWS to identify the user to impersonate.
  
Your service application identifies the user account to impersonate by using one of the following three identifiers:
  
- The primary SMTP address.
    
- The user principal name (UPN).
    
- The security identifier (SID).
    
The identifier that you use depends, of course, on the information that your application has available.
  
## Identifying the user account to impersonate

Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating. The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user. EWS uses the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment. 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

Each of the following sections shows how to use one of the identifiers. For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).
  
### Use the SMTP email address to identify the user account

The SMTP email address is the primary email address that is associated with a user account.
  
In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

In an EWS SOAP request, the [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t:PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### Use the UPN to identify the user account

The UPN contains the fully qualified domain name (FQDN) for the location of the user account. This is not necessarily the user's mailbox domain. The **UserPrincipalName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed. 
  
In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) element contains the UPN for the user account. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### Use the SID to identify the user account

The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.
  
In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

In an EWS SOAP request, the [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## See also


- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [ExchangeService class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

