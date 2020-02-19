---
title: "Authenticate an IMAP, POP or SMTP connection using OAuth"
description: "Learn how to use OAuth authentication with your IMAP, POP, and SMTP applications."
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
---

# Authenticate an IMAP, POP or SMTP connection using OAuth

Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols in Exchange Online in Office 365 and Outlook.com.

If you're not familiar with OAuth 2.0, start by reading the [Microsoft identity platform (v2.0) overview](/azure/active-directory/develop/v2-overview). That document introduces you to different components of Microsoft identity platform, including SDKs.

You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365, Outlook.com. To use OAuth with your application you will, at the minimum, need to:

1. [Register your application](#register-your-application) with Azure Active Directory.
1. [Configure your application](#configure-your-application) in Azure Active Directory.
1. [Get an access token](#get-an-access-token) from a token server.
1. [Authenticate connection requests](#authenticate-connection-requests) with an access token.

## Register your application

To use OAuth, an application must be registered with Azure Active Directory.

Follow the instructions listed in [Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to create a new application.

## Configure your application

Follow the instructions listed in [Configure a client application to access web APIs](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)

Make sure to add one or more of the following permission scopes that correspond to the protocols you would like to integrate with. In the **Add a permission** wizard, select **Microsoft Graph** and then **Delegated permissions** to find the following permission scopes listed.

| Protocol  | Permission scope        |
|-----------|-------------------------|
| IMAP      | `IMAP.AccessAsUser.All` |
| POP       | `POP.AccessAsUser.All`  |
| SMTP AUTH | `SMTP.Send`             |

## Get an access token

You can use one of our [MSAL client libraries](/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.

Alternatively, you can follow the steps listed in [OAuth2 On-Behalf-Of flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow) to call the underlying identity platform REST APIs and retrieve an access token.

## Authenticate connection requests

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
S: A01 OK Success
```

Sample client-server message exchange that results in an authentication failure:

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed
```

### POP Protocol Exchange

To authenticate a POP server connection, the client will have to respond with an `AUTH` command in the following format:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Sample client-server message exchange that results in an authentication success:

```text
[connection begins]
C: AUTH XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYX
JlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0
Q2cBAQ==
S: +OK Welcome.
[connection continues...]
```

Sample client-server message exchange that results in an authentication failure:

```text
[connection begins]
C: AUTH XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: + eyJzdGF0dXMiOiI0MDAiLCJzY2hlbWVzIjoiQmVhcmVyIiwic2NvcGUiOiJodHRwczovL21haWwuZ29vZ2xlLmNvbS8ifQ==
```

## See also

- [Authentication and EWS in Exchange](authentication-and-ews-in-exchange.md)
- [Internet Message Access Protocol](https://tools.ietf.org/html/rfc3501)
- [Post Office Protocol](https://tools.ietf.org/html/rfc1081)
