---
title: "Authenticate an IMAP, POP or SMTP connection using OAuth"
description: "Learn how to use OAuth authentication with your IMAP, POP, and SMTP applications."
author: svpsiva
ms.date: 07/08/2021
ms.audience: Developer
---

# Authenticate an IMAP, POP or SMTP connection using OAuth

Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols and access email data for Office 365 users.

> OAuth2 support for IMAP, POP, SMTP protocols as described below is supported for both Microsoft 365 (which includes Office on the web) and Outlook.com users.

If you're not familiar with the OAuth 2.0 protocol, start by reading the [OAuth 2.0 protocol on Microsoft identity platform overview](/azure/active-directory/develop/active-directory-v2-protocols). To learn more about the Microsoft Authentication Libariers (MSAL), which implement the OAuth 2.0 protocol to authenticate users and access secure APIs, read the [MSAL overview](/azure/active-directory/develop/msal-overview).

You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365. To use OAuth with your application you need to:

1. [Register your application](#register-your-application) with Azure Active Directory.
1. [Configure your application](#configure-your-application) in Azure Active Directory.
1. [Get an access token](#get-an-access-token) from a token server.
1. [Authenticate connection requests](#authenticate-connection-requests) with an access token.

## Register your application

To use OAuth, an application must be registered with Azure Active Directory.

Follow the instructions listed in [Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to create a new application.

## Get an access token

You can use one of our [MSAL client libraries](/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.

Alternatively, you can select an appropriate flow from the following list and follow the corresponding steps to call the underlying identity platform REST APIs and retrieve an access token.

1. [OAuth2 authorization code flow](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2 Device authorization grant flow](/azure/active-directory/develop/v2-oauth2-device-code)

OAuth access to IMAP, POP, SMTP AUTH protocols via OAuth2 client credentials grant flow is not supported. If your application needs persistent access to all mailboxes in a Microsoft 365 organization, we recommend that you use the Microsoft Graph APIs which allow access without a user, enable granular permissions and let administrators scope such access to a specific set of mailboxes.

Make sure to specify the full scopes, including Outlook resource URLs, when authorizing your application and requesting an access token.

| Protocol  | Permission scope string |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| SMTP AUTH | `https://outlook.office.com/SMTP.Send`             |

In addition, you can request for [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) scope. When a user approves the offline_access scope, your app can receive refresh tokens from the Microsoft identity platform token endpoint. Refresh tokens are long-lived. Your app can get new access tokens as older ones expire.

## Authenticate connection requests

You can initiate a connection to Office 365 mail servers using the [IMAP and POP email settings for Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).

### SASL XOAUTH2

OAuth integration with requires your application to use SASL XOAUTH2 format for encoding and transmitting the access token. SASL XOAUTH2 encodes the username, access token together in the following format:

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A` represents a **Control** + **A** (`%x01`).

For example, the SASL XOAUTH2 format to access `test@contoso.onmicrosoft.com` with access token `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` is:

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

After base64 encoding, this translates to the following string. Note that line breaks are inserted for readability.

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### SASL XOAUTH2 authentication for shared mailboxes in Office 365

In case of shared mailbox access using OAuth, application needs to obtain the access token on behalf of a user but replace the userName field in the SASL XOAUTH2 encoded string with the email address of the shared mailbox. 

### IMAP Protocol Exchange

To authenticate a IMAP server connection, the client will have to respond with an `AUTHENTICATE` command in the following format:

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

Sample client-server message exchange that results in an authentication success:

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

Sample client-server message exchange that results in an authentication failure:

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### POP Protocol Exchange

To authenticate a POP server connection, the client will have to respond with an `AUTH` command split into two lines in the following format:	 

```text	
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>	
```	

Sample client-server message exchange that results in an authentication success:	

```text	
[connection begins]	
C: AUTH XOAUTH2 	
S: +	
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYX	
JlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0	
Q2cBAQ==	
S: +OK User successfully authenticated.	
[connection continues...]	
```	

Sample client-server message exchange that results in an authentication failure:	

```text	
[connection begins]	
C: AUTH XOAUTH2 	
S: +	
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY	
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj	
l0Q2cBAQ=	
S: -ERR Authentication failure: unknown user name or bad password.	
```

### SMTP Protocol Exchange

To authenticate a SMTP server connection, the client will have to respond with an `AUTH` command in the following format:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Sample client-server message exchange that results in an authentication success:

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 235 2.7.0 Authentication successful
[connection continues...]
```

Sample client-server message exchange that results in an authentication failure:

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## See also

- [Authentication and EWS in Exchange](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [IMAP, POP Connection settings](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet Message Access Protocol](https://tools.ietf.org/html/rfc3501)
- [Post Office Protocol](https://tools.ietf.org/html/rfc1081)
- [SMTP Service extension for Authentication](https://tools.ietf.org/html/rfc4954)
