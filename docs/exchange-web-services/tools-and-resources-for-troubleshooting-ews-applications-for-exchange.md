---
title: "Tools and resources for troubleshooting EWS applications for Exchange" 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer 
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: "Find resources to help you troubleshoot your EWS Managed API or EWS application."
localization_priority: Priority
---

# Tools and resources for troubleshooting EWS applications for Exchange

Find resources to help you troubleshoot your EWS Managed API or EWS application.
  
Things don't always go as planned. Sometimes EWS requests fail, or provide unexpected results. This can be frustrating, especially if the reason isn't obvious. Hopefully this never happens to you, but if it does, this article provides information about tools and resources that you can use to help troubleshoot your problem.
  
> [!NOTE]
> This article provides general troubleshooting advice and sources for troubleshooting information. Unfortunately it isn't possible to give detailed troubleshooting steps. For assistance troubleshooting your specific error, see [Next steps](#bk_NextSteps). 
  
## Examine the SOAP requests and responses

When things aren't working correctly, it really helps to be able to see what's going on. The first line of inquiry when investigating a problem with EWS or the EWS Managed API is to examine the requests that your application is sending over the network and the responses that the server is sending back.
  
The EWS Managed API makes examining SOAP requests and responses easy with its [built in tracing functionality](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). If you are using EWS, you might or might not have access to similar tracing functionality, depending on what platform or classes you use to send your requests. However, you can always use a network tracing tool like [Network Monitor](https://www.microsoft.com/download/details.aspx?id=4865) or [Fiddler](http://www.telerik.com/fiddler) to examine the network traffic and view the request and response payloads. 
  
Additionally, you can [instrument your client requests](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) to enhance the information available in requests and responses. 
  
After you have the requests and responses, ask yourself the following: Do they look correct? Are the values that your application is sending expected? Do the responses make sense?
  
## Examine error codes

Sometimes the error code can go a long way toward pinpointing the problem, even if at first glance it doesn't seem to make sense. Does the error indicate that your client is being [throttled](ews-throttling-in-exchange.md)? Perhaps a call to Autodiscover to [refresh configuration information](how-to-refresh-configuration-information-by-using-autodiscover.md) is in order? 
  
For more information about handling specific errors, see the following articles:
  
- [Handling Autodiscover error messages](handling-autodiscover-error-messages.md)
    
- [Handling notification-related errors in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Handling synchronization-related errors in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Handling deletion-related errors in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## Verify versions

There are a number of different components involved in EWS operations, and the versions of those components can influence the results.
  
**Table 1. Versioned components that can affect EWS processes**

|**Component**|**EWS Managed API**|**EWS**|**Notes**|
|:-----|:-----|:-----|:-----|
|Requested server version  <br/> |[ExchangeServiceBase.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property  <br/> |[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) element  <br/> |This value controls which version of the EWS schema is used to process the EWS request. Make sure that the schema version specified here makes sense for the request you are sending. Some properties and operations are not available in earlier versions of the schema.  <br/> |
|The server version  <br/> |[ExchangeServiceBase.ServerInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) property  <br/> |[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) element  <br/> |This value is returned by the server in EWS responses, and indicates the version of the server that processed the response. Make sure this value is what you expect. If possible, make sure that the Exchange server is running the most recent update for your major version of Exchange.  <br/> |
|The EWS Managed API version  <br/> |The Product version property of the Microsoft.Exchange.WebServices.dll file.  <br/> |Not applicable  <br/> |If you're using the EWS Managed API, make sure that you are using [the most recent version](https://aka.ms/ews-managed-api-readme).  <br/> |
   
## Verify access

EWS is enabled by default, but [defaults can be changed](how-to-control-access-to-ews-in-exchange.md). Use the [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) cmdlet to make sure that EWS is enabled on the server, and the [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) cmdlet to make sure that EWS is enabled for the user's mailbox. Also check both cmdlet responses for an EWS allow or block list, and make sure that your application isn't blocked from using EWS. 
  
You should also verify that the [default authentication settings](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) on the EWS virtual directory have not been modified. 
  
## Try another EWS client

Sometimes it is helpful to try the same request from another client and compare results. If another client gets different results, what is different? Figuring out what is different between a successful request and a failed request can help explain why a particular request is failing.
  
While you can certainly write another client to test with, you don't have to! [EWSEditor](https://github.com/dseph/EwsEditor/releases) is a sample client that uses the EWS Managed API and EWS. You can download the client (including the source code) and use it to try the same requests that are failing in your application. 
  
## Examine IIS logs

If you have access to the Exchange server, the logging functionality provided by Internet Information Services (IIS) on the Client Access servers can provide more information about failures. However, keep in mind that IIS logs will only be helpful if you are receiving an HTTP error.
  
IIS provides two different logging methods: [IIS logging](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) and [failed requests tracing](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). To work with IIS logs, you can use [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), which includes a number of built-in EWS queries.
  
## Next steps
<a name="bk_NextSteps"> </a>

Now that you've learned about the tools and resources that you can use to troubleshoot, you might need help understanding the information provided by those tools. The following are some options for getting help:
  
- [Exchange Server Development forum on Q&A](/answers/topics/192527/office-exchange-server-dev.html) — Ask a question of the Q&A Exchange Server development community. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) — Ask a question of the StackOverflow community. Be sure to tag your post with "ews". 
    
- [Microsoft Support](https://support.microsoft.com/ph/730/en-us) — Contact a Microsoft support professional for assistance. 
    
## See also


See the following articles:
  
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Trace requests and responses to troubleshoot EWS Managed API applications](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Instrumenting client requests for EWS and REST in Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [EWS throttling in Exchange](ews-throttling-in-exchange.md)
    
- [Refresh configuration information by using Autodiscover](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Handling Autodiscover error messages](handling-autodiscover-error-messages.md)
    
- [Handling notification-related errors in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Handling synchronization-related errors in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Handling deletion-related errors in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Configuring Logging in IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Troubleshooting Failed Requests Using Tracing in IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Introducing: Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Default Settings for Exchange Virtual Directories](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
Download the following:
  
- [Microsoft Network Monitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Web Services Managed API](https://www.nuget.org/packages/Microsoft.Exchange.WebServices/)
