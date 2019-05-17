---
title: "Authenticate an EWS application by using OAuth"
manager: sethgros
ms.date: 05/17/2019
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

2. [Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.

3. [Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.

> [!NOTE]
> OAuth authentication for EWS is only available in Exchange as part of Office 365. EWS applications that use OAuth must be registered with Azure Active Directory.

To use the code in this article, you will need to have access to the following:

- An Office 365 account with an Exchange Online mailbox. If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.

- The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).

- The [EWS Managed API](https://github.com/officedev/ews-managed-api).

## Register your application

To use OAuth, an application must have an application ID issued by Azure Active Directory. In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.

1. Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.

1. Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.

1. Select **New registration**. On the **Register an application** page, set the values as follows.

    - Set **Name** to a friendly name for your app.
    - Set **Supported account types** to the choice that makes sense for your scenario.
    - For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.

1. Choose **Register**. On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.

## Add code to get an authentication token

The following code shows how to use the Microsoft Authentication Library to get an authentication token. It assumes that the information required to make the authentication request is stored in the application's **App.config** file. This example does not include error checking, see the [Code sample](#code-sample) for the complete code.

```cs
// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

## Add an authentication token to EWS requests

After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

## Code sample

The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }

        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

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
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

The sample code requires an **App.config** file with the following entries:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- If you registered your app to support only users in your organization, change the value
           of this key to your tenant ID -->
    <add key="tenantId" value="common"/>
  </appSettings>
</configuration>
```

## See also

- [Authentication and EWS in Exchange](authentication-and-ews-in-exchange.md)
