---
title: "Trace requests and responses to troubleshoot EWS Managed API apps"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: "Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application."
localization_priority: Priority
---

# Trace requests and responses to troubleshoot EWS Managed API apps

Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.
  
Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to. Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error. 
  
If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue. If you're using the EWS Managed API, you don't have direct access to the EWS request and response. However, you can use tracing methods on the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working. 

For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error. The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application. If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request. 
  
## Enabling tracing on the ExchangeService object
<a name="bk_EnableTracing"> </a>

To enable tracing, create an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example. 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

After you set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener. You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**. You can use the [TraceFlags enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses. 
  
## Implementing a TraceListener object
<a name="bk_traceListener"> </a>

You can set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window. If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) object. The following code example shows a simple object that implements the [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files. 
  
```cs
class TraceListener : ITraceListener
{
    #region ITraceListener Members
    public void Trace(string traceType, string traceMessage)
    {
      CreateXMLTextFile(traceType, traceMessage.ToString());
    }
    #endregion
    private void CreateXMLTextFile(string fileName, string traceContent)
    {
      // Create a new XML file for the trace information.
      try
      {
        // If the trace data is valid XML, create an XmlDocument object and save.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.Load(traceContent);
        xmlDoc.Save(fileName + ".xml");
      }
      catch
      {
        // If the trace data is not valid XML, save it as a text document.
        System.IO.File.WriteAllText(fileName + ".txt", traceContent);
      }
    }
}

```

## See also

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [Handling Autodiscover error messages](handling-autodiscover-error-messages.md)    
- [Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md)    
- [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

