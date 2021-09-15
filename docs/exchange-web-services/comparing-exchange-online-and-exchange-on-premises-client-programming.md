---
title: "Comparing Exchange Online and Exchange on-premises client programming"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: "Learn about the design considerations for creating an EWS Managed API or EWS client application that works against Exchange Online and Exchange on-premises."
---

# Comparing Exchange Online and Exchange on-premises client programming

Learn about the design considerations for creating an EWS Managed API or EWS client application that works against Exchange Online and Exchange on-premises.
  
For the most part, clients and the web services in Exchange they target will work the same way regardless of whether the target is an Exchange Online, Exchange Online as part of Office 365, or Exchange on-premises server. There are, however, some exceptions, and you'll want to make sure that your application can handle them. Use the information in this article to help you design your client to target both Exchange Online and Exchange on-premises.

<a name="autodiscover"> </a>

## Autodiscover client programming considerations

[Autodiscover](autodiscover-for-exchange.md) provides configuration information for Exchange clients. A client application can discover its configuration information in one of three ways, depending on whether the client is targeting Exchange Online or Exchange on-premises. 
  
**Table 1. Autodiscover service types and Exchange applicability**

|**Autodiscover service type**|**Applies to**|
|:-----|:-----|
|[SOAP Autodiscover](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online and versions of Exchange on-premises starting with Exchange 2010  <br/> |
|[POX Autodiscover](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online and versions of Exchange on-premises starting with Exchange 2007  <br/> |
|[Service connection point (SCP) lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Versions of Exchange on-premises starting with Exchange 2007  <br/> |
   
In addition to the client configuration information, that SOAP and POX Autodiscover also return the Exchange service version and indicate whether the service is hosted by Exchange Online. This information is returned in different elements, depending on the type of Autodiscover you use.
  
**Table 2. Autodiscover elements that return service version and Exchange Online hosting information**

|**Autodiscover service type**|**XML element that contains service version**|**XML element that indicates whether the user has an Exchange Online account**|
|:-----|:-----|:-----|
|SOAP Autodiscover  <br/> |[Setting (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element with the **CasVersion** text value.  <br/> |[Setting (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element with the **UserMSOnline** text value.  <br/> |
|POX Autodiscover  <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Ensure that your client captures this information so that it can target the [feature set](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) that is available on the Exchange server. This can be useful to determine whether your client can expect different behavior based on whether the user's mailbox is located in an Exchange Online or Exchange on-premises organization. 

<a name="testing"> </a>

## Testing and log files in applications that target Exchange Online

Exchange Online does not provide access to the EWS protocol log files, EWS performance counters, and EWS-related service events that are available on on-premises Exchange servers. Access to these is useful, however, in discovering how your application performs when it interacts with EWS. Make sure that you test your application against a test Exchange on-premise server so that you can optimize its performance. If possible, you can [change the throttling settings](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies) on your test server to match the throttling settings for Exchange Online, so you can evaluate how your application will behave when it connects to Exchange Online. 
  
> [!TIP]
> You can use the [EWSRelentless](https://ewsrelentless.codeplex.com/) tool to perform an EWS load test. You can use this tool with a test server, the EWS protocol logs, EWS performance counters, service events, and the EWS throttling settings to better understand how EWS performs under load. 

<a name="throttling"> </a>

## Throttling settings and Exchange Online

The default values for the [EWS throttling settings](ews-throttling-in-exchange.md) are different for Exchange Online than they are for Exchange on-premises. Also, you cannot change Exchange Online throttling settings. You can use Exchange Management Shell cmdlets to discover the throttling settings for Exchange on-premises; however, those cmdlets are not enabled for Exchange Online. 

<a name="ems"> </a>

## Exchange Management Shell cmdlets and configuration settings

A number of cmdlets can directly or indirectly affect the web service APIs in Exchange Online and Exchange on-premises. Cmdlets are not available for the following in Exchange Online:
  
- Throttling settings 
    
- Virtual directory settings 
    
- Authentication settings
    
For details about the cmdlets that are available for Exchange Online, see [PowerShell cmdlets in Exchange Online](http://help.outlook.com/140/dd575549.aspx). For more about cmdlets that are available for Exchange on-premises, see [Exchange 2013 cmdlets](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx).
  
## Client affinity and network load balancers
<a name="affinity"> </a>

Most EWS communication does not require that the client participate in maintaining affinity with Exchange. The subscriptions to mailbox events do require that the client provide cookies and other information to maintain affinity with the Exchange server that maintains the queue of mailbox events for a user. Exchange Server 2010 uses the exchangecookie to maintain client affinity across the network load balancers. Exchange Online and versions of Exchange on-premises starting with Exchange 2013 use the [X-AnchorMailbox header, X-PreferServerAffinity header, and X-BackEndOverrideCookie cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) to maintain affinity for mailbox notifications. 
  
## Authentication
<a name="auth"> </a>

Clients can authenticate with Exchange Online by using either Basic or OAuth. Versions of Exchange on-premises starting with Exchange 2013 use NTLM by default; however, it's possible to configure Exchange on-premises to use Basic authentication as well. 
  
## Client latency diagnostics
<a name="diag"> </a>

Exchange Online collects client latency diagnostics if they are reported. This helps Microsoft support troubleshoot connectivity issues with Exchange Online. Exchange on-premises does not collect client latency diagnostics. If your client targets Exchange on-premises, the client can't report latency diagnostics to the server.
  
## Functionality in the EWS Managed API
<a name="ewsma"> </a>

The EWS Managed API exposes some functionality that is specific to Exchange on-premises, such as service point connection lookup, and some functionality that is specific to Exchange Online, such as client latency reporting. Note that it's possible for some functionality to be implemented in Exchange Online before it is implemented in the EWS Managed API. 
  
The following EWS Managed API functionality is only applicable to Exchange Online:
  
- Client latency reporting
    
- Basic pre-authentication
    
- The ability to request that the RequestId be returned in responses
    
## API features in Exchange Online plans and Exchange Server editions
<a name="exo"> </a>

Different feature sets might be available in different Office 365 and Exchange Online plans, or in the standard and enterprise versions of Exchange Server. Be aware that some API functionality might not be available to your client application depending on the Exchange Online plan or Exchange Server edition that hosts a user's mailbox. 
   
Because feature availability can change, we recommend that you check the Exchange Online plans and Exchange Server editions to evaluate how feature availability might affect your client. You can also design your client to check feature availability by using the [GetServiceConfiguration operation](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) or by sending test requests for the operations that implement the features. If the feature isn't available, the response from the server will indicate as such. 
  
## Other considerations
<a name="other"> </a>

You can do the following when targeting Exchange on-premises but not Exchange Online:
  
- Create a client that is installed on the Exchange server. 
    
- Install [custom transport agents](../transport-agents/transport-agents-in-exchange-2013.md) that can affect the delivery and content of messages you create and send with EWS and other clients. 
    
## See also

- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
- [Comparing Exchange Online and Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Compare all Office 365 for business plans](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless - EWS load generation tool](https://ewsrelentless.codeplex.com/)
- [Web service API feature availability in Exchange and the EWS Managed API](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [EWS throttling in Exchange](ews-throttling-in-exchange.md)
    

