---
title: "Get started with EWS Managed API client applications"
manager: sethgros
ms.date: 01/22/2022
ms.audience: Developer
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: "Develop a simple Hello World email client application for Exchange by using the EWS Managed API."
localization_priority: Priority
---

# Get started with EWS Managed API client applications

Develop a simple Hello World email client application for Exchange by using the EWS Managed API.
  
The [EWS Managed API](https://aka.ms/ews-managed-api-readme) provides an intuitive, easy-to-use object model for sending and receiving web service messages from client applications, portal applications, and service applications. You can access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or an Exchange server mailbox by using the EWS Managed API. You can use the information in this article to help you develop your first EWS Managed API client application.

> [!NOTE]
> We’re removing the ability to use Basic authentication in Exchange Online for EWS beginning October 2022: [Deprecation of Basic authentication in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). You should use OAuth authentication instead. [Authenticate an EWS application by using OAuth](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth)
  
> [!NOTE]
> The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api). You can use the open source library to:
>
> - Contribute bug fixes and enhancements to the API.
> - Get fixes and enhancements before they are available in an official release.
> - Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.
>
> We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/main/CONTRIBUTING.md) on GitHub.
  
## You'll need an Exchange server

If you already have an Exchange mailbox account, you can skip this section. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS client application:
  
- Get an [Office 365 Developer Site](https://msdn.microsoft.com/library/office/fp179924.aspx) (recommended). This is the quickest way for you to set up an Exchange mailbox.

- Download [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).

After you have verified that you can send and receive email from Exchange, you are ready to set up your development environment. You can use the Exchange web client [Outlook Web App](https://technet.microsoft.com/library/jj657718%28v=exchg.150%29.aspx) to verify that you can send email.
  
## Set up your development environment

Make sure that you have access to the following:
  
- Any version of [Visual Studio](https://www.visualstudio.com/downloads/download-visual-studio-vs.aspx) that supports the .NET Framework 4. Although technically, you don't need Visual Studio because you can use any C# compiler, we recommend that you use it.

- The [EWS Managed API](https://aka.ms/ews-managed-api-readme). You can use either the 64-bit or 32-bit version, depending on your system. Use the default installation location.

## Create your first EWS Managed API application

These steps assume that you set up an Office 365 Developer Site. If you downloaded and installed Exchange, you will need to [install a valid certificate](https://technet.microsoft.com/library/bb310769%28v=exchg.141%29.aspx) on your Exchange server or [implement a certificate validation](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) callback for a self-signed certificate that is provided by default. Also note that these steps might vary slightly depending on the version of Visual Studio that you are using.
  
### Step 1: Create a project in Visual Studio

1. In Visual Studio, on the **File** menu, choose **New**, and then choose **Project**. The **New Project** dialog box opens.

2. Create a **C# Console Application**. From the **Templates** pane, choose **Visual C#**, and then choose **Console Application**.

3. Name the project HelloWorld, and then choose **OK**.

Visual Studio creates the project and opens the Program.cs code document window.

### Step 2: Add a reference to the EWS Managed API

1. If the **Solution Explorer** window is already open, skip this step and proceed to step 2. To open the **Solution Explorer** window, on the **View** menu, choose **Solution Explorer**.

2. In the **Solution Explorer** and the **HelloWorld** project, open the shortcut menu (right-click) for **References** and choose **Add Reference** from the context menu. A dialog box for managing project references will open.

3. Choose the **Browse** option. Browse to the location where you installed the EWS Managed API DLL. The default path set by the installer is the following: C:\Program Files\Microsoft\Exchange\Web Services\<version>. The path can vary based on whether you download the 32 or 64 bit version of the Microsoft.Exchange.WebServices.dll. Choose **Microsoft.Exchange.WebServices.dll** and select **OK** or **Add**. This adds the EWS Managed API reference to your project.

4. If you are using EWS Managed API 2.0, change the HelloWorld project to target the .NET Framework 4. Other versions of the EWS Managed API might use a different target version of the .NET Framework.

5. Confirm that you are using the correct target version of the .NET Framework. Open the shortcut menu (right-click) for your **HelloWorld** project in the **Solution Explorer**, and choose **Properties**. Verify that the **.NET Framework 4** is selected in the **Target framework** drop-down box.

Now that you have your project set up and you created a reference to the EWS Managed API, you are ready to create your first application. To keep things simple, add your code to the Program.cs file. Read [Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md) for more information about referencing the EWS Managed API. In the next step, you will develop the basic code to write most EWS Managed API client applications.]

### Step 3: Set up URL redirection validation for Autodiscover

- Add the following redirection validation callback method after the **Main(string[] args)** method. This validates whether redirected URLs returned by [Autodiscover](autodiscover-for-exchange.md) represent an HTTPS endpoint.

  ```cs
  private static bool RedirectionUrlValidationCallback(string redirectionUrl)
  {
     // The default for the validation callback is to reject the URL.
     bool result = false;
     Uri redirectionUri = new Uri(redirectionUrl);
     // Validate the contents of the redirection URL. In this simple validation
     // callback, the redirection URL is considered valid if it is using HTTPS
     // to encrypt the authentication credentials. 
     if (redirectionUri.Scheme == "https")
     {
        result = true;
     }
     return result;
  }
  ```

This validation callback will be passed to the **ExchangeService** object in step 4. You need this so that your application will trust and follow Autodiscover redirects - the results of the Autodiscover redirect provides the EWS endpoint for our application.

### Step 4: Prepare the ExchangeService object

1. Add a **using** directive reference to the EWS Managed API. Add the following code after the last **using** directive at the top of Program.cs.

   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. In the **Main** method, instantiate the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object with the service version you intend to target. This example targets the earliest version of the EWS schema.

   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. If you are targeting an on-premises Exchange server and your client is domain joined, proceed to step 4. If you client is targeting an Exchange Online or Office 365 Developer Site mailbox, you have to pass explicit credentials. Add the following code after the instantiation of the **ExchangeService** object and set the credentials for your mailbox account. The user name should be the user principal name. Proceed to step 5.

   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. Domain-joined clients that target an on-premises Exchange server can use the default credentials of the user who is logged on, assuming the credentials are associated with a mailbox. Add the following code after the instantiation of the **ExchangeService** object.

   ```cs
    service.UseDefaultCredentials = true;
   ```

   If your client targets an Exchange Online or Office 365 Developer Site mailbox, verify that [UseDefaultCredentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) is set to **false**, which is the default value. Your client is ready to make the first call to the Autodiscover service to get the service URL for calls to the EWS service.

5. The **AutodiscoverUrl** method on the **ExchangeService** object performs a series of calls to the Autodiscover service to get the service URL. If this method call is successful, the URL property on the **ExchangeService** object will be set with the service URL. Pass the user's email address and the **RedirectionUrlValidationCallback** to the **AutodiscoverUrl** method. Add the following code after the credentials have been specified in step 3 or 4. Change `user1@contoso.com` to your email address so that the Autodiscover service finds your EWS endpoint.

   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

At this point, your client is set up to make calls to EWS to access mailbox data. If you run your code now, you can verify that the **AutodiscoverUrl** method call worked by examining the contents of the [ExchangeService.Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) property. If this property contains a URL, your call was a success! This means that your application successfully authenticated with the service and discovered the EWS endpoint for your mailbox. Now you are ready to make your first calls to EWS. Read [Set the EWS service URL by using the EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) for more information about setting the EWS URL.

### Step 6: Create your first Hello World email message

1. After the **AutodiscoverUrl** method call, instantiate a new **EmailMessage** object and pass in the service object you created.

   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   You now have an email message on which the service binding is set. Any calls initiated on the **EmailMessage** object will be targeted at the service.

2. Now set the To: line recipient of the email message. To do this, change `user1@contoso.com` to use your SMTP address.

   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. Set the subject and the body of the email message.

   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. You are now ready to send your first email message by using the EWS Managed API. The **Send** method will call the service and submit the email message for delivery. Read [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) to learn about other methods you can use to communicate with Exchange.

   ```cs
    email.Send();
   ```

5. You are ready to run your Hello World application. In Visual Studio, select **F5**. A blank console window will open. You will not see anything in the console window while your application authenticates, follows Autodiscover redirections, and then makes its first call to create an email message that you send to yourself. If you want to see the calls being made, add the following two lines of code before the **AutodiscoverUrl** method is called. Then press F5. This will [trace out the EWS requests and responses](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) to the console window.

   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

You now have a working EWS Managed API client application. For your convenience, the following example shows all the code that you added to Program.cs to create your Hello World application.

```cs
using System;
using Microsoft.Exchange.WebServices.Data;
namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
      service.Credentials = new WebCredentials("user1@contoso.com", "password");
      service.TraceEnabled = true;
      service.TraceFlags = TraceFlags.All;
      service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
      EmailMessage email = new EmailMessage(service);
      email.ToRecipients.Add("user1@contoso.com");
      email.Subject = "HelloWorld";
      email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API");
      email.Send();
    }
    private static bool RedirectionUrlValidationCallback(string redirectionUrl)
    {
      // The default for the validation callback is to reject the URL.
      bool result = false;
      Uri redirectionUri = new Uri(redirectionUrl);
      // Validate the contents of the redirection URL. In this simple validation
      // callback, the redirection URL is considered valid if it is using HTTPS
      // to encrypt the authentication credentials. 
      if (redirectionUri.Scheme == "https")
      {
        result = true;
      }
      return result;
    }
  }
}
```

## Next steps

If you're ready to do more with your first EWS Managed API client application, explore the following resources:
  
- [Exchange 2013: 101 code samples](https://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)
- [Folders and items](folders-and-items-in-ews-in-exchange.md)
- [EWSEditor](http://ewseditor.codeplex.com/)

If you run into any issues with your application, [try posting a question or comment in the forum](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) (and don't forget to read the top post).
  
## In this section

- [Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md)
- [Set the EWS service URL by using the EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)
- [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)

## See also

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
- [Trace requests and responses to troubleshoot EWS Managed API applications](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
