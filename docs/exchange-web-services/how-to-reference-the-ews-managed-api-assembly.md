---
title: "Reference the EWS Managed API assembly"
manager: sethgros
ms.date: 01/22/2022
ms.audience: Developer
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: "Find information about how to reference the EWS Managed API assembly."
localization_priority: Priority
---

# Reference the EWS Managed API assembly

Find information about how to reference the EWS Managed API assembly.
  
The EWS Managed API provides a simple and full-featured interface for developing and extending applications that use Exchange Web Services (EWS). Whether you are using Visual Studio or another code editor to develop your EWS Managed API application, you will need to make a reference to the EWS Managed API assembly. If you haven't installed the EWS Managed API already, be sure to [download the API](https://aka.ms/ews-managed-api-readme).
  
> [!NOTE]
> The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api). You can use the open source library to:
>
> - Contribute bug fixes and enhancements to the API.
> - Get fixes and enhancements before they are available in an official release.
> - Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.
>
> We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/main/CONTRIBUTING.md) via GitHub.
  
## Referencing the assembly

The most common way to add a reference is to use Visual Studio. We know that some developers out there like to use other editors, so we are including instructions for using the command-line compiler as well as instructions for using Visual Studio. You might notice that the code examples that follow have the same **using** statements. The difference between the two methods is that the command-line compiler needs the location of the assembly file. The Visual Studio reference handles this for you behind the scenes.
  
### To add a reference by using Visual Studio

1. Put the Microsoft.Exchange.WebServices.dll file and the Microsoft.Exchange.WebServices.xml file into a folder of your choice. By default, the files are installed in `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, but you can store the files anywhere on your computer.
2. In the Solution Explorer pane in Visual Studio, select **References**, and then choose **Add Reference**. This opens the Add Reference window.
3. In the Add Reference window, navigate to the **Browse** tab, browse to the location of the Microsoft.Exchange.WebServices.dll file, select that file, and then select **OK**.
4. To use the EWS Managed API in your application, add a **using** statement for the **Microsoft.Exchange.WebServices.Data** namespace.

   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### To add a reference and build your application with the command-line compiler

1. Put the Microsoft.Exchange.WebServices.dll file into a folder of your choice. This folder will be the output folder for the compiler.
2. In your source code editor, add a **using** statement to the source code for the **Microsoft.Exchange.WebServices.Data** namespace.

   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. Run the command-line compiler to build the application. The following command uses the .NET Framework C# compiler to build the Windows application defined in the source code file "program.cs". It assumes that the compiler is located in the default installation directory and that the Microsoft.Exchange.WebServices.dll file is in a subdirectory of the current directory named "build".

   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## See also

- [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md)
- [Setting up your Exchange application development environment](setting-up-your-exchange-application-development-environment.md)
- [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
