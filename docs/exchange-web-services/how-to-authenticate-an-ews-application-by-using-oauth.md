---
title: "Authenticate an EWS application by using OAuth"
manager: sethgros
ms.date: 11/25/2020
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: "Learn how to use OAuth authentication with your EWS Managed API applications."
localization_priority: Priority
---

<!-- markdownlint-disable MD025 -->
# Authenticate an EWS application by using OAuth
<!-- markdownlint-enable MD025 -->

Learn how to use OAuth authentication with your EWS Managed API applications.

You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365. To use OAuth with your application you will need to:

1. [Register your application](#register-your-application) with Azure Active Directory.
1. [Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.
1. [Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.

> [!NOTE]
> OAuth authentication for EWS is only available in Exchange Online as part of Microsoft 365. EWS applications that use OAuth must be registered with Azure Active Directory.

To use the code in this article, you will need to have access to the following:

- A Microsoft 365 account with an Exchange Online mailbox. If you do not have a Microsoft 365 account, you can [sign up for the Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) to get a free Microsoft 365 subscription.
- The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client).
- The [EWS Managed API](https://github.com/officedev/ews-managed-api).

There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online. Before you proceed with the tutorial, you will need to choose the specific permission type to use.

- **Delegated permissions** are used by apps that have a signed-in user present. For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.
- **Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.

## Register your application

To use OAuth, an application must have an application ID issued by Azure Active Directory. In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory. You can register an application in the Azure Active Directory admin center or by using Microsoft Graph.

1. Open a browser and navigate to the [Microsoft Entra admin center](https://entra.microsoft.com) and login using a **Work or School Account**.

1. Select **Identity** in the left-hand navigation, then select **App registrations** under **Applications**.

1. Select **New registration**. On the **Register an application** page, set the values as follows.

    - Set **Name** to a friendly name for your app.
    - Set **Supported account types** to the choice that makes sense for your scenario.
    - For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `https://login.microsoftonline.com/common/oauth2/nativeclient`.

1. Choose **Register**. On the next page, copy the values of the **Application (client) ID** and **Directory (tenant) ID** and save them, you will need them later.

> [!NOTE]
> Developers can log in with a work or school account to register an app in an Entra ID directory, or log in with a personal account (MSA) that is a guest in an Entra ID directory.
> If developers do not have an Entra ID directory, they can get one for free from the M365 Developer Program.

### Configure for delegated authentication

If your application uses delegated authentication, no further configuration is required. The [Microsoft identity platform](/azure/active-directory/develop/v2-overview) allows apps to request permissions dynamically, so you do not have to pre-configure permissions on the app registration. However, in some scenarios (like the [on-behalf-of flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) pre-configuring permissions is required. Use the following steps to pre-configure EWS permissions.

1. Select **Manifest** in the left-hand navigation under **Manage**.

1. Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
                "type": "Scope"
            }
        ]
    }
    ```

1. Select **Save**.

1. Select **API permissions** under **Manage**. Confirm that the **EWS.AccessAsUser.All** permission is listed.

### Configure for app-only authentication

To use application permissions, follow these additional steps.

1. Select **Manifest** in the left-hand navigation under **Manage**.

1. Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
                "type": "Role"
            }
        ]
    }
    ```

1. Select **Save**.

1. Select **API permissions** under **Manage**. Confirm that the **full_access_as_app** permission is listed.

1. Select **Grant admin consent for org** and accept the consent dialog.

1. Select **Certificates & Secrets** in the left-hand navigation under **Manage**.

1. Select **New client secret**, enter a short description and select **Add**.

1. Copy the **Value** of the newly added client secret and save it, you will need it later.

## Add code to get an authentication token

The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions. These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file. These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.

### Get a token with delegated auth

```cs
// Using Microsoft.Identity.Client 4.22.0

// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### Get a token with app-only auth

```cs
// Using Microsoft.Identity.Client 4.22.0
var cca = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
    .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
    .Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

//Make the token request
var authResult = await cca.AcquireTokenForClient(ewsScopes).ExecuteAsync();
```

## Add an authentication token to EWS requests

After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

To use application permissions, you will also need to explicitly impersonate a mailbox that you would like to access.

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## Code samples

### Delegated authentication

The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using delegated authentication.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0

            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            // The permission scope required for EWS access
            var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

            try
            {
                // Make the interactive token request
                var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

### App-only authentication

The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using app-only authentication.

> [!NOTE]
> When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP address of the impersonated mailbox.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0
            var cca = ConfidentialClientApplicationBuilder
                .Create(ConfigurationManager.AppSettings["appId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
                .Build();

            var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

            try
            {
                var authResult = await cca.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
                ewsClient.ImpersonatedUserId =
                    new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "meganb@contoso.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "meganb@contoso.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

The sample code in both cases requires an **App.config** file with the following entries:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- The tenant ID copied from your app registration -->
    <add key="tenantId" value="YOUR_TENANT_ID_HERE"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## See also

- [Authentication and EWS in Exchange](authentication-and-ews-in-exchange.md)
- [What to do with EWS Managed API PowerShell scripts that use Basic Authentication](https://github.com/gscales/EWS-BasicToOAuth-Info/blob/main/What%20to%20do%20with%20EWS%20Managed%20API%20PowerShell%20scripts%20that%20use%20Basic%20Authentication.md)
