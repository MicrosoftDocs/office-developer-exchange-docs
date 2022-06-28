---
title: "Authenticate an IMAP, POP or SMTP connection using OAuth"
description: "Learn how to use OAuth authentication with your IMAP, POP, and SMTP applications."
author: svpsiva
ms.date: 09/21/2021
ms.audience: Developer
---

# Authenticate an IMAP, POP or SMTP connection using OAuth

Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols and access email data for Office 365 users.

> OAuth2 support for IMAP, POP, SMTP protocols as described below is supported for both Microsoft 365 (which includes Office on the web) and Outlook.com users.

If you're not familiar with the OAuth 2.0 protocol, start by reading the [OAuth 2.0 protocol on Microsoft identity platform overview](/azure/active-directory/develop/active-directory-v2-protocols). To learn more about the Microsoft Authentication Libraries (MSAL), which implement the OAuth 2.0 protocol to authenticate users and access secure APIs, read the [MSAL overview](/azure/active-directory/develop/msal-overview).

You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365. To use OAuth with your application you need to:

1. [Register your application](#register-your-application) with Azure Active Directory.
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

## Using client credentials grant flow to authenticate IMAP and POP connections

Exchange service principals are used to enable applications to access Exchange mailboxes with client credentials flow with the POP and IMAP protocols.

### Add the POP and IMAP permissions to your AAD application

1. Select the **API Permissions** blade in your AAD application's management view in the Azure Portal.

2. Click **Add permission**.

3. Click the **APIs my organization uses** tab and search for "*Office 365 Exchange Online*".

4. Click **Application permissions**.

5. For POP access, select the **POP.AccessAsApp** permission. For IMAP access, select the **IMAP.AccessAsApp** permission.

   ![pop-imap-permission](media/pop-imap-api-permissions.png)

6. Once selected, click **Add permissions**.

You should now have the POP or IMAP application permissions added to your AAD application's permissions.

### Get tenant admin consent

For each tenant you would like to access Exchange mailboxes via POP or IMAP, your AAD application must get tenant admin consent. Learn more about [tenant admin consent process](/azure/active-directory/develop/v2-permissions-and-consent) here.

In your OAuth 2.0 tenant authorization request, the `scope` query parameter should be `https://ps.outlook.com/.default` for both the POP and IMAP application scopes.

Your OAuth 2.0 authorization request URL should look something like this:

```
https://login.microsoftonline.com/{tenant}/v2.0/adminconsent?client_id=CLIENT_ID_HERE&redirect_uri=REDIRECT_URI_HERE&scope=https://ps.outlook.com/.default
```

### Registering service principals in Exchange

Once your AAD application is consented by a tenant admin, the tenant admin must register your AAD application's service principal in Exchange via Exchange Online PowerShell. This is enabled by the `New-ServicePrincipal` cmdlet. (TODO: Link to New-ServicePrincipal cmdlet reference when released)

Here is an example of registering an AAD application's service principal in Exchange:

```
New-ServicePrincipal –Identity <Service principal object ID in AAD> -AppId <Application ID in AAD> [-Organization <Org ID>]
```

Your tenant admin can now add the specific mailboxes in the tenant that will be allowed to be access by your application. This is done with the [`Add-MailboxPermission` cmdlet](/powershell/module/exchange/add-mailboxpermission).

Here is an example of giving your application access to one mailbox:

```text
Add-MailboxPermission -Identity "john.smith@contoso.com" -User 
"<SERVICE_PRINCIPAL_ID>" -AccessRights FullAccess
```

Your AAD application can now access the allowed mailboxes via the POP or IMAP protocols using OAuth client credentials tokens. [Instructions on on how to generate OAuth client credentials tokens can be found here](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow).

You must use `https://outlook.office365.com/.default` in the `scope` property in the body payload for the access token request.

The access tokens generated can be used to authenticate POP and IMAP connections via SASL XOAUTH2 as described earlier in this page.

## See also

- [Authentication and EWS in Exchange](../exchange-web-services/authentication-and-ews-in-exchange.md)

- [IMAP, POP Connection settings](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)

- [Internet Message Access Protocol](https://tools.ietf.org/html/rfc3501)

- [Post Office Protocol](https://tools.ietf.org/html/rfc1081)

- [SMTP Service extension for Authentication](https://tools.ietf.org/html/rfc4954)
