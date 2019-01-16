---
title: "Authenticate an EWS application by using OAuth"
manager: sethgros
ms.date: 01/15/2019
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: "Learn how to use OAuth authentication with your EWS Managed API applications."
---

# Authenticate an EWS application by using OAuth

Learn how to use OAuth authentication with your EWS Managed API applications.
  
You can use the OAuth authentication service provided by Azure Active Directory to integrate your EWS Managed API applications with the same authentication model used by the Office 365 REST APIs. To use OAuth with your application you will need to:
  
1. [Register your application](#bk_register) with Azure Active Directory. 
    
2. [Add code to get an authentication token](#bk_getToken) to get an authentication token from a token server. 
    
3. [Add an authentication token to EWS requests](#bk_useToken) that you send. 
    
> [!NOTE]
> OAuth authentication for EWS is only available in Exchange as part of Office 365. EWS applications must be registered with Azure Active Directory, and require the "Access mailboxes as the signed-in user via Exchange Web Services" permission of "Office 365 Exchange Online (Microsoft.Exchange)". 
  
To use the code in this article, you will need to have access to the following:
  
- An [Office 365 developer account](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program). You can use a trial account to test your application.
    
- The [Azure AD Authentication Library for .NET](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries).
    
- [The EWS Managed API](https://github.com/officedev/ews-managed-api).

<a name="bk_register"> </a>

## Register your application

To use OAuth, an application must have a client identifier and an application URI that identifies the application. If you have not yet registered your application with Azure Active Directory Services, you'll need to manually add your application by following the steps at [Register an app](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-v1-add-azure-ad-app). 

In this tutorial, it is assumed that the application is a console application, so you need to register your application as a native application with Azure Active Directory. And you need to grant the "Access mailboxes as the signed-in user via Exchange Web Services" permission of "Office 365 Exchange Online (Microsoft.Exchange)" to your application. 

<a name="bk_getToken"> </a>

## Add code to get an authentication token

The Azure AD Authentication Library for .NET simplifies getting an authentication token from Azure Active Directory so that you can use the token in your application. You need to provide four pieces of information to get the token:
  
1. The URI of the token server. The token server is the **authority** that authenticates the user and returns a token that your application can use to access EWS. 
    
2. The application client ID created when you registered your application with Azure Active Directory.
    
3. The application client URI created when you registered your application with Azure Active Directory.
    
4. The URI of the EWS server and the URI of the EWS endpoint. For Exchange as part of Office 365, this will be `https://outlook.office365.com/EWS/Exchange.asmx`.
    
The following code shows how to use the Azure AD Authentication Library to get an authentication token. It assumes that the information required to make the authentication request is stored in the application's App.config file. This example does not include error checking, see the [Code sample](#bk_codeSample) for the complete code. 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"]);
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireTokenAsync(serverName, clientID, clientAppUri, new PlatformParameters(PromptBehavior.Always)).Result;
```

<a name="bk_useToken"> </a>

## Add an authentication token to EWS requests

After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service. 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013_SP1);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"] + "EWS/Exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken);
exchangeService.FindFolders(WellKnownFolderName.Root, new FolderView(10));
```

<a name="bk_codeSample"> </a>

## Code sample

The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request.
  
```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using System;
using System.Configuration;
using System.Threading;

namespace TestV1App
{
    class Program
    {
        static void Main(string[] args)
        {
            var t = new Thread(Run);
            t.SetApartmentState(ApartmentState.STA);
            t.Start();
            t.Join();
        }

        static void Run()
        {
            string authority = ConfigurationManager.AppSettings["authority"];
            string clientID = ConfigurationManager.AppSettings["clientID"];
            Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"]);
            string serverName = ConfigurationManager.AppSettings["serverName"];
            AuthenticationResult authenticationResult = null;
            AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);

            string errorMessage = null;

            try
            {
                Console.WriteLine("Trying to acquire token");
                authenticationResult = authenticationContext.AcquireTokenAsync(serverName, clientID, clientAppUri, new PlatformParameters(PromptBehavior.Always)).Result;
            }
            catch (AdalException ex)
            {
                errorMessage = ex.Message;
                if (ex.InnerException != null)
                {
                    errorMessage += "\nInnerException : " + ex.InnerException.Message;
                }
            }
            catch (ArgumentException ex)
            {
                errorMessage = ex.Message;
            }

            if (!string.IsNullOrEmpty(errorMessage))
            {
                Console.WriteLine("Failed: {0}" + errorMessage);
                return;
            }

            Console.WriteLine("\nMaking the protocol call\n");
            ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013_SP1);
            exchangeService.Url = new Uri(serverName + "EWS/Exchange.asmx");
            exchangeService.TraceEnabled = true;
            exchangeService.TraceFlags = TraceFlags.All;
            exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken);
            exchangeService.FindFolders(WellKnownFolderName.Root, new FolderView(10));
        }
    }
}
```

The sample code requires an App.config file with the following entries:
  
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup> 
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
  </startup>
  <appSettings>
    <add key="authority" value="https://login.windows.net/common" />
    <add key="clientID" value="Application ID generated by Azure Active Directory"/>
    <add key="clientAppUri" value="Sign-on URL registered with Azure Active Directory"/>
    <add key="serverName" value="https://outlook.office365.com/" />
  </appSettings>
</configuration>
```

## See also

- [Authentication and EWS in Exchange](authentication-and-ews-in-exchange.md)    

    

