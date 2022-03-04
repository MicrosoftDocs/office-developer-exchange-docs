---
title: "Improving performance when using Autodiscover for Exchange"
 
 
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: e65ff6b2-3810-43ad-9728-27308891b193
description: "Learn about ways to improve the performance of the Autodiscover process in your application."
---

# Improving performance when using Autodiscover for Exchange

Learn about ways to improve the performance of the Autodiscover process in your application.
  
There are a lot of reasons to like Autodiscover. Configuring your application to connect to Exchange with no user intervention is great! If you're reading this article, you probably already know all the reasons to use and love Autodiscover, so we won't list them here. Instead, we're going to talk about a potential downside: performance.
  
Autodiscover isn't inherently a slow process, but it's not inherently fast either. The [Autodiscover process](autodiscover-for-exchange.md) involves a lot of network activity, and that introduces a lot of potential for delays. The Autodiscover process has three phases; all three have the potential to affect performance: 
  
- Defining the Autodiscover endpoint candidate pool — For applications running on domain-joined computers, this can involve [SCP lookups](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md), which involves communicating with Active Directory Domain Services (AD DS).
    
- Trying each candidate — This requires an HTTP request/response to each candidate endpoint.
    
- Trying other alternatives — When the candidates in your Autodiscover endpoint candidate pool don't produce results, you can do an unauthenticated GET request (HTTP request/response) and a DNS lookup.
    
On the surface this might not seem like much. However, imagine a scenario where the Autodiscover endpoint candidate pool is more than one or two URLs, and you don't find a working one until the last URL in your pool. The delay can become a bit more noticeable. So, what can you do?
  
## Consider the need for SCP lookup

When SCP objects are present and configured well, they can speed up the Autodiscover process. In other situations, however, they can slow it down. If SCP isn't used in your environment, skip the entire SCP lookup portion of the Autodiscover process to save time.
  
The EWS Managed API makes this easy: just set the [ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx) property to **false** before calling the [ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method. If you're using the [AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx) class, set the [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx) property to **false** before calling any of its methods. 
  
## Use Autodiscover less often

Autodiscover isn't designed to be used frequently use by applications. The intent behind Autodiscover is for an application to use it to discover configuration information, and then cache that information for a period of time. If you aren't caching configuration information, consider adding caching to your application to reduce the number of times you use Autodiscover.
  
Even if you are already caching, evaluate how long you cache configuration information. The standard is to [refresh Autodiscover information every 24 hours](how-to-refresh-configuration-information-by-using-autodiscover.md), but you might be able to extend that time. You should test with your target environments and come up with a "time-to-live" for your configuration that works for you.
  
## Minimize requested data

If you're using the **AutodiscoverService** class in the EWS Managed API, or the [GetUserSettings operation (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) operation via SOAP, you have direct control over what settings are returned in the response. Although you can request quite a few settings, chances are that your application only needs a handful of them. Every setting that you request requires more processing on the server, which means more time waiting for a response. Evaluate the settings you are requesting, and eliminate any that you don't need. 
  
If you're using the **ExchangeService.AutodiscoverUrl** method in the EWS Managed API, you cannot change the settings you request. However, this method is already fairly efficient; it only requests the **ExternalEwsUrl** and **InternalEwsUrl** settings from the [UserSettingName enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx).
  
If you're using the POX Autodiscover service, [you cannot request specific properties](autodiscover-for-exchange.md#bk_Options).
  
## See also


- [Autodiscover for Exchange](autodiscover-for-exchange.md)
    
- [Find Autodiscover endpoints by using SCP lookup in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Refresh configuration information by using Autodiscover](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [ExchangeService class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)
    
- [AutodiscoverService class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)
    

