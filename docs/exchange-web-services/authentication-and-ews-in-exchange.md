---
title: "Authentication and EWS in Exchange"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: "Find information to help you choose the right authentication standard for your EWS application that targets Exchange."
localization_priority: Priority
---

# Authentication and EWS in Exchange

Find information to help you choose the right authentication standard for your EWS application that targets Exchange.
  
Authentication is a key part of your Exchange Web Services (EWS) application. Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013 support standard web authentication protocols to help secure the communication between your application and the Exchange server.
  
If you're targeting Exchange Online, the authentication method that you choose must use HTTPS to encrypt the requests and responses that your application sends. Although you can use HTTP with Exchange on-premises servers, we recommend that you use HTTPS for any request that your application sends to an EWS endpoint to help secure communication between your application and an Exchange server.
  
Exchange provides the following authentication options for you to choose from: 
  
- OAuth 2.0 (Exchange Online only)
    
- NTLM (Exchange on-premises only)
    
- Basic (no longer recommended)
    
The authentication method that you choose depends on the security requirements of your organization, whether you are using Exchange Online or Exchange on-premises, and whether you have access to a third-party provider that can issue OAuth tokens. This article provides information that will help you select the authentication standard that's right for your application.
  
## OAuth authentication

We recommend that all new applications use the OAuth standard to connect to Exchange Online services. The advantage in security over basic authentication is worth the additional work required to implement OAuth in your application. For the record, however, there are also some disadvantages that you should be aware of.
  
**Table 1. Advantages and disadvantages of using OAuth**

|**Advantages**|**Disadvantages**|
|:-----|:-----|
| OAuth is an industry-standard authentication protocol.<br/><br/>Authentication is managed by a third-party provider. Your application does not have to collect and store the Exchange credentials.<br/><br/>Fewer worries for you, because your application only receives an opaque token from the authentication provider; therefore, a security breach in your application can only expose the token, not the user's Exchange credentials.  <br/> | OAuth relies on a third-party authentication provider. This can impose additional costs on your organization or your customers.<br/><br/>The OAuth standard is more difficult to implement than basic authentication.<br/><br/>To implement OAuth, you need to integrate your application with both the authentication provider and the Exchange server.  <br/> |
   
To help minimize the disadvantages, you can use the [Microsoft Azure AD Authentication Library](/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) to authenticate users to Active Directory Domain Services (AD DS) in the cloud or on-premises and then obtain access tokens for securing calls to an Exchange server. Exchange Online requires tokens issued by the Azure Active Directory service, which is supported by the ADAL; however, you can use any third-party library. 
  
To learn more about using OAuth authentication in your EWS application, see the following resources:
  
- [Office 365 trial](/office/developer-program/microsoft-365-developer-program), to set up an Exchange server to use to test your client application.
    
- [Azure AD Authentication Library for .NET](/azure/active-directory/azuread-dev/active-directory-authentication-libraries)
    
- [Configure Azure Active Directory](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx), to enable your application to use OAuth tokens for authentication.
    
- Review the sample code in [Authenticate an EWS application by using OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md) for example code that you can study. 
    
## NTLM authentication

NTLM authentication is only available for Exchange on-premises servers. For applications that run inside the corporate firewall, integration between NTLM authentication and the .NET Framework provides a built-in means to authenticate your application. 
  
**Table 2. Advantages and disadvantages of using NTLM authentication**

|**Advantages**|**Disadvantages**|
|:-----|:-----|
| Works "out of the box" with your Exchange server. You can configure access to Exchange services by using an [Exchange Management Shell cmdlet](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Uses the .NET Framework [CredentialCache](https://msdn2.microsoft.com/library/615e0wsd) object to automatically get the user's credentials.<br/><br/>[Code samples are available](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) that use the logged on user's credentials for authentication to an on-premises Exchange server.  <br/> | Users must be logged on to a domain to use NTLM authentication.<br/><br/>It can be difficult to access email accounts that are not associated with the user's domain account.<br/><br/>Service applications must have a domain account to take advantage of NTLM authentication.  <br/> |

   
## Basic authentication

Basic authentication provides a, well, basic level of security for your client application. We do recommend that all new applications use either NTLM or the OAuth protocol for authentication; however, basic authentication can be the correct choice for your application in some circumstances.
  
**Table 3. Advantages and disadvantages of using basic authentication**

|**Advantages**|**Disadvantages**|
|:-----|:-----|
| Works "out of the box" with your Exchange server. You can configure access to Exchange services by using an [Exchange Management Shell cmdlet](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Windows applications can use the logged on user's default credentials.<br/><br/>Many [code samples are available](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) that show you how to call EWS using basic authentication.  <br/> | Requires your application to collect and store the user's credentials.<br/><br/>You have to turn off NTLM authentication if you want to force all users to use basic authentication.<br/><br/>If a security breach occurs in your application, it can expose the user's email address and password to the attacker.  <br/> |
   
You need to decide if basic authentication meets the security requirements of your organization and customers. Basic authentication can be the right choice if you want to avoid extensive setup tasks, for example for simple test or demonstration applications.

> [!NOTE]
> Basic authentication is no longer supported for EWS to connect to Exchange Online. Use OAuth authentication in all your new or existing EWS applications to connect to Exchange Online. OAuth authentication for EWS is only available in Exchange Online as part of Microsoft 365. EWS applications that use OAuth must be registered with Azure Active Directory first.
  
## See also
- [Authenticate an EWS application by using OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md)
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)   
- [Adding Sign-On to Your Web Application Using Microsoft Azure AD](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [Control access to EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)    
- [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Supported token and claim types](https://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
