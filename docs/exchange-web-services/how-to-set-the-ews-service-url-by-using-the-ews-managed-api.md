---
title: "Set the EWS service URL by using the EWS Managed API"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: cddf6525-1c04-484b-a911-56c2f0f1f7b6
description: "Find information about how to set the EWS service URL in your EWS Managed API application."
localization_priority: Priority
---

# Set the EWS service URL by using the EWS Managed API

Find information about how to set the EWS service URL in your EWS Managed API application.
  
The service URL is the address that Exchange uses to communicate with Exchange Web Services (EWS). After your EWS Managed API application has this address, and has appropriate access to [communicate with EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), it can make calls to the [ExchangeService class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). The service URL for an on-premises Exchange server might look like the following. 
  
```HTML
https://computer.domain.contoso.com/EWS/Exchange.asmx
```

You can set the EWS URL in your application in a couple of ways. We recommend that you use the [Autodiscover service](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) to get the URL because in a large forest of servers, the URL can change if the mailbox is migrated to another server. However, because calling Autodiscover can take some time and can slow down your application if you need to make multiple calls in a short period of time, you might want to cache the URL value you get from Autodiscover and manually set the EWS service URL with this cached value. This will improve the performance of your application; just make sure that you use Autodiscover to update your cached value periodically in case the value changes on the server. 
  
## Set the EWS service URL by using the Autodiscover service
<a name="bk_SetURLusingAutoDiscover"> </a>

The [AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method uses the email address to set the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) endpoint and enables your application to use any methods included in the **ExchangeService** proxy classes. The following example shows how to use the **AutodiscoverURL** method. 
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.AutodiscoverUrl("User1@contoso.com");

```

## Set the Exchange service URL manually
<a name="bk_SetURLmanually"> </a>

The following example shows you how to set the EWS service URL by using a cached value. Before you do this, make sure to use the Autodiscover service to get the EWS URL.
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.Url = new Uri("https://computername.domain.contoso.com/EWS/Exchange.asmx");

```

## See also

- [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md)   
- [Setting up your Exchange application development environment](setting-up-your-exchange-application-development-environment.md)   
- [Control access to EWS in Exchange](how-to-control-access-to-ews-in-exchange.md) 
- [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)  
- [Use Autodiscover to find connection points](how-to-use-autodiscover-to-find-connection-points.md)
    

