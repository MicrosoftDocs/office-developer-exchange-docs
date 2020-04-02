---
title: "Authenticate an IMAP, POP or SMTP connection using OAuth"
description: "Learn how to use OAuth authentication with your IMAP, POP, and SMTP applications."
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
---

# Authenticate an IMAP, POP or SMTP connection using OAuth

Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols in Exchange Online in Office 365 and Outlook.com.

If you're not familiar with OAuth 2.0, start by reading the [Microsoft identity platform (v2.0) overview](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-overview). That document introduces you to different components of Microsoft identity platform, including SDKs.

You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365, Outlook.com. To use OAuth with your application you will, at the minimum, need to:

1. [Register your application](#register-your-application) with Azure Active Directory.
1. [Configure your application](#configure-your-application) in Azure Active Directory.
1. [Get an access token](#get-an-access-token) from a token server.
1. [Authenticate connection requests](#authenticate-connection-requests) with an access token.

## Register your application

To use OAuth, an application must be registered with Azure Active Directory.

Follow the instructions listed in [Register an application with the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) to create a new application.

## Configure your application

Follow the instructions listed in [Configure a client application to access web APIs](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis)

Make sure to add one or more of the following permission scopes that correspond to the protocols you would like to integrate with. In the **Add a permission** wizard, select **Microsoft Graph** and then **Delegated permissions** to find the following permission scopes listed.

| Protocol  | Permission scope        |
|-----------|-------------------------|
| IMAP      | `IMAP.AccessAsUser.All` |
| POP       | `POP.AccessAsUser.All`  |
| SMTP AUTH | `SMTP.Send`             |

## Get an access token

You can use one of our [MSAL client libraries](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.

Alternatively, you can select an appropriate flow from the following list and follow the corresponding steps to call the underlying identity platform REST APIs and retrieve an access token. 
1. [OAuth2 authorization code flow](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2 implicit grant flow](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-implicit-grant-flow)
1. [OAuth2 Device authorization grant flow](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-device-code)

Make sure to specify the full scopes, including Outlook resource URL's, when authorizing your application and requesting an access token. 

| Protocol  | Permission scope string |
|-----------|-------------------------|
| IMAP      | `https://outlook.office365.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office365.com/POP.AccessAsUser.All`  |
| SMTP AUTH | `https://outlook.office365.com/SMTP.Send`             |

## Authenticate connection requests

You can initiate a connection to Office 365 mail servers using the [IMAP and POP email settings for Office 365](https://support.office.com/en-us/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353) 

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

### SMTP Protocol Exchange

To authenticate a SMTP server connection, the client will have to respond with an `AUTH` command in the following format:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Sample client-server message exchange that results in an authentication success:

```text
[connection begins]
auth xoauth2
334
dXNlcj1qb25qb25AYmVsbHJlZC5vcmcBYXV0aD1iZWFyZXIgZXlKMGVYQWlPaUpLVjFRaUxDSnViMjVqWlNJNkltaFViemRVV2tKaFpUTkJSSEZoWTNOM1ZubHZZV0Y0UnpFNFZYUmhZbHBmVHpWMVN6TmlkbGRVVDJjaUxDSmhiR2NpT2lKU1V6STFOaUlzSW5nMWRDSTZJbGxOUlV4SVZEQm5kbUl3YlhodlUwUnZXV1p2YldweFptcFpWU0lzSW10cFpDSTZJbGxOUlV4SVZEQm5kbUl3YlhodlUwUnZXV1p2YldweFptcFpWU0o5LmV5SmhkV1FpT2lKb2RIUndjem92TDI5MWRHeHZiMnN1YjJabWFXTmxNelkxTG1OdmJTSXNJbWx6Y3lJNkltaDBkSEJ6T2k4dmMzUnpMbmRwYm1SdmQzTXVibVYwTHpOa05qWXhZemRtTFdZME5qUXROR05pWWkxaFl6VTJMV1ZtTmpZeE1UWTVaalJtTUM4aUxDSnBZWFFpT2pFMU9EVTNPREkxTkRrc0ltNWlaaUk2TVRVNE5UYzRNalUwT1N3aVpYaHdJam94TlRnMU56ZzJORFE1TENKaFkyTjBJam93TENKaFkzSWlPaUl4SWl3aVlXbHZJam9pUVZSUlFYa3ZPRkJCUVVGQmFUWkhNemhpYzNsV1JYRm1lVTgyWVVOclYxUmhlVzhyUkhSSU1qQTNXRXhGVDNaSlZuSmtUbFZFWlhJNVMxaEJjbkF3UjFVMGNXTTFTMUZyZW5NMmR5SXNJbUZ0Y2lJNld5SndkMlFpWFN3aVlYQndYMlJwYzNCc1lYbHVZVzFsSWpvaVIzSmhjR2hVWlhOMFFYQndNaUlzSW1Gd2NHbGtJam9pWm1KallqRTROVFF0WkRWa09TMDBZamN3TFRneFpqZ3RNR1l5TmpBMU16VTRPVE5sSWl3aVlYQndhV1JoWTNJaU9pSXhJaXdpWlc1bWNHOXNhV1J6SWpwYlhTd2labUZ0YVd4NVgyNWhiV1VpT2lKS2IyNWxjeUlzSW1kcGRtVnVYMjVoYldVaU9pSktiMjRpTENKcGNHRmtaSElpT2lJM015NHlOVFF1TVRJeUxqRXlNaUlzSW01aGJXVWlPaUpLYjI0Z1NtOXVaWE1pTENKdmFXUWlPaUl3TlROaE9XRXpPQzA1TkRrMkxUUXlaV1l0WWpWbU5DMWlOelptWmpjM09UaGpaR0VpTENKd2RXbGtJam9pTVRBd016QXdNREJCTkVZMU9VRkJRaUlzSW5OamNDSTZJa2xOUVZBdVFXTmpaWE56UVhOVmMyVnlMa0ZzYkNCVFRWUlFMbE5sYm1RaUxDSnphV1FpT2lKa1l6ZzNZVEJrWVMwNE1qSTRMVFJsTURFdE9XWXpOaTAyTWpnNE9HRXdOREV6TW1NaUxDSnpkV0lpT2lKNFRtUkxkSFJCWDFaT1UxWkVPVlJtUTNWNVRsRkdabTFMT0VWUldIZENVREZ5Vm1KRVF6a3RMVzVOSWl3aWRHbGtJam9pTTJRMk5qRmpOMll0WmpRMk5DMDBZMkppTFdGak5UWXRaV1kyTmpFeE5qbG1OR1l3SWl3aWRXNXBjWFZsWDI1aGJXVWlPaUpLYjI1S2IyNUFZbVZzYkhKbFpDNXZjbWNpTENKMWNHNGlPaUpLYjI1S2IyNUFZbVZzYkhKbFpDNXZjbWNpTENKMWRHa2lPaUl0TkRkTlkyVjBUVGhyUTBGTVVWZzBkRkpOUmtGQklpd2lkbVZ5SWpvaU1TNHdJbjAuWG1MSHl0RGhsa0J4eE1YWHN3amJVOG5PQjRFRjFYRDRUdlNtS2RNLUV5X2RWbkpXd0ZwZVpmeXcxUU9OSnFnM3lTdjRfTUJzVnNaYXJ5Q3BqNldQS2hSeXZFdU1SSFQwS3NDZzRTVXEtLXNGS0c3S1dzQTNkdEg1U3NxbXcxbjRtQWwzVFJoWld0Qmk4dGpVWWlDUXhfbVNPWGtHYnNXTWFpXzBkRjlYM3VpVUxKVDNTVG00ekZURlMxeVEzcjVfWHgyMXY0aTJwRWJQVjlUenE4YU85MmZqSFNheHFUWjZfT0NRN0RFSUxfekgtbWtZWXU3eXRjZWtIVkgzVmtlMlRfRENIUVNSdm9ZTWNpYlNWNGVaNnVDYTdINmtBaUtwZ3B4QmMydHZIblhsdGZOb3d2T1JDdnVGZlRQV2tOckRKQ2g2M1pCcWFiRHNHc3VFY2VSNzdnAQE=
235 2.7.0 Authentication successful
[connection continues...]
```

Sample client-server message exchange that results in an authentication failure:

```text
[connection begins]
auth xoauth2
334
dXNlcj1qb25qb25AYmVsbHJlZC5jb20BYXV0aD1iZWFyZXIgZXlKMGVYQWlPaUpLVjFRaUxDSnViMjVqWlNJNkltaFViemRVV2tKaFpUTkJSSEZoWTNOM1ZubHZZV0Y0UnpFNFZYUmhZbHBmVHpWMVN6TmlkbGRVVDJjaUxDSmhiR2NpT2lKU1V6STFOaUlzSW5nMWRDSTZJbGxOUlV4SVZEQm5kbUl3YlhodlUwUnZXV1p2YldweFptcFpWU0lzSW10cFpDSTZJbGxOUlV4SVZEQm5kbUl3YlhodlUwUnZXV1p2YldweFptcFpWU0o5LmV5SmhkV1FpT2lKb2RIUndjem92TDI5MWRHeHZiMnN1YjJabWFXTmxNelkxTG1OdmJTSXNJbWx6Y3lJNkltaDBkSEJ6T2k4dmMzUnpMbmRwYm1SdmQzTXVibVYwTHpOa05qWXhZemRtTFdZME5qUXROR05pWWkxaFl6VTJMV1ZtTmpZeE1UWTVaalJtTUM4aUxDSnBZWFFpT2pFMU9EVTNPREkxTkRrc0ltNWlaaUk2TVRVNE5UYzRNalUwT1N3aVpYaHdJam94TlRnMU56ZzJORFE1TENKaFkyTjBJam93TENKaFkzSWlPaUl4SWl3aVlXbHZJam9pUVZSUlFYa3ZPRkJCUVVGQmFUWkhNemhpYzNsV1JYRm1lVTgyWVVOclYxUmhlVzhyUkhSSU1qQTNXRXhGVDNaSlZuSmtUbFZFWlhJNVMxaEJjbkF3UjFVMGNXTTFTMUZyZW5NMmR5SXNJbUZ0Y2lJNld5SndkMlFpWFN3aVlYQndYMlJwYzNCc1lYbHVZVzFsSWpvaVIzSmhjR2hVWlhOMFFYQndNaUlzSW1Gd2NHbGtJam9pWm1KallqRTROVFF0WkRWa09TMDBZamN3TFRneFpqZ3RNR1l5TmpBMU16VTRPVE5sSWl3aVlYQndhV1JoWTNJaU9pSXhJaXdpWlc1bWNHOXNhV1J6SWpwYlhTd2labUZ0YVd4NVgyNWhiV1VpT2lKS2IyNWxjeUlzSW1kcGRtVnVYMjVoYldVaU9pSktiMjRpTENKcGNHRmtaSElpT2lJM015NHlOVFF1TVRJeUxqRXlNaUlzSW01aGJXVWlPaUpLYjI0Z1NtOXVaWE1pTENKdmFXUWlPaUl3TlROaE9XRXpPQzA1TkRrMkxUUXlaV1l0WWpWbU5DMWlOelptWmpjM09UaGpaR0VpTENKd2RXbGtJam9pTVRBd016QXdNREJCTkVZMU9VRkJRaUlzSW5OamNDSTZJa2xOUVZBdVFXTmpaWE56UVhOVmMyVnlMa0ZzYkNCVFRWUlFMbE5sYm1RaUxDSnphV1FpT2lKa1l6ZzNZVEJrWVMwNE1qSTRMVFJsTURFdE9XWXpOaTAyTWpnNE9HRXdOREV6TW1NaUxDSnpkV0lpT2lKNFRtUkxkSFJCWDFaT1UxWkVPVlJtUTNWNVRsRkdabTFMT0VWUldIZENVREZ5Vm1KRVF6a3RMVzVOSWl3aWRHbGtJam9pTTJRMk5qRmpOMll0WmpRMk5DMDBZMkppTFdGak5UWXRaV1kyTmpFeE5qbG1OR1l3SWl3aWRXNXBjWFZsWDI1aGJXVWlPaUpLYjI1S2IyNUFZbVZzYkhKbFpDNXZjbWNpTENKMWNHNGlPaUpLYjI1S2IyNUFZbVZzYkhKbFpDNXZjbWNpTENKMWRHa2lPaUl0TkRkTlkyVjBUVGhyUTBGTVVWZzBkRkpOUmtGQklpd2lkbVZ5SWpvaU1TNHdJbjAuWG1MSHl0RGhsa0J4eE1YWHN3amJVOG5PQjRFRjFYRDRUdlNtS2RNLUV5X2RWbkpXd0ZwZVpmeXcxUU9OSnFnM3lTdjRfTUJzVnNaYXJ5Q3BqNldQS2hSeXZFdU1SSFQwS3NDZzRTVXEtLXNGS0c3S1dzQTNkdEg1U3NxbXcxbjRtQWwzVFJoWld0Qmk4dGpVWWlDUXhfbVNPWGtHYnNXTWFpXzBkRjlYM3VpVUxKVDNTVG00ekZURlMxeVEzcjVfWHgyMXY0aTJwRWJQVjlUenE4YU85MmZqSFNheHFUWjZfT0NRN0RFSUxfekgtbWtZWXU3eXRjZWtIVkgzVmtlMlRfRENIUVNSdm9ZTWNpYlNWNGVaNnVDYTdINmtBaUtwZ3B4QmMydHZIblhsdGZOb3d2T1JDdnVGZlRQV2tOckRKQ2g2M1pCcWFiRHNHc3VFY2VSNzdnAQE=
535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```
## See also

- [Authentication and EWS in Exchange](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [IMAP, POP Connection settings](https://support.office.com/en-us/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet Message Access Protocol](https://tools.ietf.org/html/rfc3501)
- [Post Office Protocol](https://tools.ietf.org/html/rfc1081)
