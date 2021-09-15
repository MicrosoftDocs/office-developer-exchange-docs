---
title: "Instrumenting client requests for EWS and REST in Exchange"
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: "Learn about the HTTP headers in EWS and REST requests and responses that can help you monitor and troubleshoot your Exchange application."
---

# Instrumenting client requests for EWS and REST in Exchange

Learn about the HTTP headers in EWS and REST requests and responses that can help you monitor and troubleshoot your Exchange application.
  
Has this ever happened to you? A user of your application reports an unexpected error. You want to investigate, but you can't reproduce it. The error has disappeared for the user, and you're left with very little actionable data. Frustrating, isn't it? Let's look at how you can proactively prepare for this scenario and hopefully avoid frustration in the future.
  
## Add instrumentation to requests

We recommend that you add additional HTTP headers to your requests to facilitate troubleshooting. You should keep a record of this information somewhere (for example, in a log file) so that you can retrieve it later if you need to. This is helpful when examining network traffic, and is also helpful if you contact Microsoft support for assistance.
  
**Table 1. Request headers for troubleshooting**

|**HTTP header (EWS)**|**EWS Managed API equivalent**|**Notes**|
|:-----|:-----|:-----|
|User-Agent  <br/> |[ExchangeService.UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Set this to a unique value that identifies your client application.<br/><br/> Using the same value for all requests that your application sends allows Microsoft to help troubleshoot call failures, should they arise.  <br/> |
|client-request-id  <br/> |[ExchangeService.ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Set this to a different unique value for every request your application sends.<br/><br/> We recommend that you use a GUID. This unique identifier is intended to be used to correlate activities between two systems in the event that something goes wrong.  <br/> |
|return-client-request-id  <br/> |[ExchangeService.ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Set this to **true** to signal to the Exchange server that it should return the value of your client-request-id in the corresponding response.<br/><br/> You can use this to correlate requests and responses in network traces or EWS Managed API traces.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Used to [report EWS latencies](#bk_ReportLatency) to Microsoft if your application is accessing Exchange Online or Exchange Online as part of Office 365.  <br/> |
   
## Log information from responses

Just as your client can add additional instrumentation to the requests it sends, Exchange adds additional instrumentation to the responses in the form of HTTP headers. Your client should capture this information to go along with the request instrumentation information.
  
> [!NOTE]
> If you are using the EWS Managed API, there is no direct equivalent for the HTTP headers. However, all HTTP response headers can be accessed via the [ExchangeService.HttpResponseHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) property. 
  
**Table 2. HTTP response headers**

|**HTTP header**|**Description**|
|:-----|:-----|
|request-id  <br/> |A server-generated ID for the request that corresponds to this response.  <br/> |
|client-request-id  <br/> |The value of the client-request-id header in the request.<br/><br/> This header is only present if the request contains the return-client-request-id header with a value of **true**.  <br/> |
|X-FEServer  <br/> |The FQDN of the Client Access server that processed the request.  <br/> |
|X-TargetBEServer  <br/> |The FQDN of the mailbox server that processed the request.  <br/> |
|X-DiagInfo  <br/> |Additional diagnostic information, depending on the request.  <br/> |
|x-ms-diagnostics  <br/> | This header is only applicable if OAuth authentication is used in the request.<br/><br/> It contains an explicit error code that specifies why an OAuth authentication failed.<br/><br/> It takes the following format: `errorId;reason="reason"error_type="error type"`<br/><br/> The **reason** field is a human-readable description of the error.<br/><br/> The **errorId** field is an integer, and the **error\_type** field is the string representation of that integer, as follows:<ul><li>2000000: invalid\_signature</li><li>2000001: invalid\_token</li><li>  2000002: token\_expired</li><li>2000003: invalid\_resource</li><li>2000004: invalid\_tenant  </li><li>2000005: invalid\_user</li><li>2000006: invalid\_client</li><li>2000007: internal\_error</li><li>2000008: invalid\_grant</li></ul> |
   
## Report EWS latency to Microsoft
<a name="bk_ReportLatency"> </a>

If your application uses the EWS Managed API or EWS to connect to Exchange Online, you can report latency in EWS requests directly to Microsoft. The information is passed via the X-ClientStatistics request header. If you are using the EWS Managed API, all you have to do is set the [ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) property to **true**. If you are using EWS, you'll need to measure the time between issuing a request and receiving a response, then add the X-ClientStatistics header to the next EWS request your application sends, using the following format.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
We maintain reports for these latencies and use them to continuously improve EWS services in Exchange Online.
  
## Next steps
<a name="bk_ReportLatency"> </a>

After you've added client instrumentation to your application, you're better prepared if something goes wrong. If that happens, you can use your instrumentation data to [troubleshoot your application](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md).
  
## See also

- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
- [Trace requests and responses to troubleshoot EWS Managed API applications](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Tools and resources for troubleshooting EWS applications for Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

